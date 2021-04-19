---
description: 寫入效果需要您瞭解效果語法，並產生必要的狀態資訊。 您可以新增著色器狀態、材質和取樣器狀態，以及您的應用程式在效果中所需的所有管線狀態。
ms.assetid: 361dd260-526a-4484-8dc9-3857874e5023
title: '將效果寫入 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e0f456c5a2bce66f782b4da7d426de5c86bbb33
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973536"
---
# <a name="writing-an-effect-direct3d-9"></a><span data-ttu-id="fd9fc-104">將效果寫入 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="fd9fc-104">Writing an Effect (Direct3D 9)</span></span>

<span data-ttu-id="fd9fc-105">寫入效果需要您瞭解效果語法，並產生必要的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="fd9fc-105">Writing an effect requires that you understand effect syntax, and generate the required state information.</span></span> <span data-ttu-id="fd9fc-106">您可以新增著色器狀態、材質和取樣器狀態，以及您的應用程式在效果中所需的所有管線狀態。</span><span class="sxs-lookup"><span data-stu-id="fd9fc-106">You can add shader state, texture and sampler state, and all of the pipeline state that your application requires in an effect.</span></span>

<span data-ttu-id="fd9fc-107">效果語法在 [ (Direct3D 9) 的效果格式 ](dx9-graphics-reference-effects-file-format.md)中有詳細的說明。</span><span class="sxs-lookup"><span data-stu-id="fd9fc-107">The effect syntax is detailed in the [Effect Format (Direct3D 9)](dx9-graphics-reference-effects-file-format.md).</span></span> <span data-ttu-id="fd9fc-108">效果通常會封裝到效果檔案中， ( fx) 但也可以撰寫為應用程式中的文字字串。</span><span class="sxs-lookup"><span data-stu-id="fd9fc-108">An effect is typically encapsulated into an effect file (.fx) but could also be written as a text string in an application.</span></span>

## <a name="effect-example"></a><span data-ttu-id="fd9fc-109">效果範例</span><span class="sxs-lookup"><span data-stu-id="fd9fc-109">Effect Example</span></span>

<span data-ttu-id="fd9fc-110">效果包含三種狀態類型：著色器狀態、材質和取樣器狀態，以及管線狀態。</span><span class="sxs-lookup"><span data-stu-id="fd9fc-110">Effects contain three types of state: shader state, texture and sampler state, and pipeline state.</span></span> <span data-ttu-id="fd9fc-111">以下是來自 [BasicHLSL 範例](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx)的效果範例：</span><span class="sxs-lookup"><span data-stu-id="fd9fc-111">Here is an example of an effect from the [BasicHLSL Sample](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx):</span></span>


```
// Global variables
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
int g_nNumLights;

float3 g_LightDir[3];               // Light's direction in world space
float4 g_LightDiffuse[3];           // Light's diffuse color
float4 g_LightAmbient;              // Light's ambient color

texture g_MeshTexture;              // Color texture for mesh

float    g_fTime;                   // App's time in seconds
float4x4 g_mWorld;                  // World matrix for object
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix
// Texture samplers
sampler MeshTextureSampler = 
sampler_state
{
    Texture = <g_MeshTexture>;
    MipFilter = LINEAR;
    MinFilter = LINEAR;
    MagFilter = LINEAR;
};
struct VS_OUTPUT
{
    float4 Position   : POSITION;   // vertex position 
    float2 TextureUV  : TEXCOORD0;  // vertex texture coords 
    float4 Diffuse    : COLOR0;     // vertex diffuse color
};
VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
    VS_OUTPUT Output;
    float3 vNormalWorldSpace;
  
    float4 vAnimatedPos = vPos;
    
    // Animation the vertex based on time and the vertex's object space position
    if( bAnimate )
        vAnimatedPos += float4(vNormal, 0) * (sin(g_fTime+5.5)+0.5)*5;
    
    // Transform the position from object space to homogeneous projection space
    Output.Position = mul(vAnimatedPos, g_mWorldViewProjection);
    
    // Transform the normal from object space to world space    
    vNormalWorldSpace = normalize(mul(vNormal, (float3x3)g_mWorld));
    
    // Compute simple directional lighting equation
    float3 vTotalLightDiffuse = float3(0,0,0);
    for(int i=0; i < nNumLights; i++ )
        vTotalLightDiffuse += g_LightDiffuse[i] * max(0,dot(vNormalWorldSpace, g_LightDir[i]));
        
    Output.Diffuse.rgb = g_MaterialDiffuseColor * vTotalLightDiffuse + 
                         g_MaterialAmbientColor * g_LightAmbient;   
    Output.Diffuse.a = 1.0f; 
    
    // Just copy the texture coordinate through
    if( bTexture ) 
        Output.TextureUV = vTexCoord0; 
    else
        Output.TextureUV = 0; 
    
    return Output;    
}
struct PS_OUTPUT
{
    float4 RGBColor : COLOR0;  // Pixel color    
};
PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                         uniform bool bTexture ) 
{ 
    PS_OUTPUT Output;

    // Lookup mesh texture and modulate it with diffuse
    if( bTexture )
        Output.RGBColor = tex2D(MeshTextureSampler, In.TextureUV) * In.Diffuse;
    else
        Output.RGBColor = In.Diffuse;

    return Output;
}
technique RenderSceneWithTexture1Light
{
    pass P0
    {          
        VertexShader = compile vs_1_1 RenderSceneVS( 1, true, true );
        PixelShader  = compile ps_1_1 RenderScenePS( true ); 
    }
}
```



<span data-ttu-id="fd9fc-112">此效果包含：</span><span class="sxs-lookup"><span data-stu-id="fd9fc-112">This effect contains:</span></span>

-   <span data-ttu-id="fd9fc-113">著色器狀態，這是與頂點著色器和圖元著色器相關聯的所有狀態。</span><span class="sxs-lookup"><span data-stu-id="fd9fc-113">The shader state, which is all of the state associated with the vertex shader and pixel shader.</span></span> <span data-ttu-id="fd9fc-114">這是由頂點和圖元著色器函式、它們所需的任何全域變數及其輸入和輸出資料結構所定義，這些都列在這裡：</span><span class="sxs-lookup"><span data-stu-id="fd9fc-114">This is defined by the vertex and pixel shader functions, any global variables they require, and their input and output data structures, all of which are listed here:</span></span>

    ```
    struct VS_OUTPUT
    {  ...  };
    VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                             ...
    {  ...  }

    struct PS_OUTPUT
    {  ...  };
    PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                             uniform bool bTexture ) 
    {  ...  }
    ```

    

-   <span data-ttu-id="fd9fc-115">材質和取樣器狀態，也就是紋理物件和取樣器物件的全域變數：</span><span class="sxs-lookup"><span data-stu-id="fd9fc-115">Texture and sampler state, which are the global variables for the texture object and the sampler object:</span></span>

    ```
    texture g_MeshTexture;              // Color texture for mesh

    sampler MeshTextureSampler = 
    sampler_state
    {
       ...
    };
    ```

    

-   <span data-ttu-id="fd9fc-116">其他效果狀態。</span><span class="sxs-lookup"><span data-stu-id="fd9fc-116">The other effect state.</span></span> <span data-ttu-id="fd9fc-117">此範例中未明確使用任何其他效果狀態。</span><span class="sxs-lookup"><span data-stu-id="fd9fc-117">There is no other effect state explicitly used in this example.</span></span> <span data-ttu-id="fd9fc-118">如果有的話，這會是它所套用之傳遞的內部技術：</span><span class="sxs-lookup"><span data-stu-id="fd9fc-118">If there were, it would be the technique inside of the pass to which it applied:</span></span>

    ```
    technique RenderSceneWithTexture1Light
    {
        pass P0
        {          
            // Any other effect state can be set here.

            VertexShader = compile vs_1_1 RenderSceneVS( 1, true, true );
            PixelShader  = compile ps_1_1 RenderScenePS( true ); 
        }
    }
    
    ```

    

## <a name="effects-contain-one-or-more-techniques-and-passes"></a><span data-ttu-id="fd9fc-119">效果包含一或多個技術與通過</span><span class="sxs-lookup"><span data-stu-id="fd9fc-119">Effects Contain One or More Techniques and Passes</span></span>

<span data-ttu-id="fd9fc-120">效果轉譯選項是藉由新增技術和傳遞來控制。</span><span class="sxs-lookup"><span data-stu-id="fd9fc-120">Effect rendering options are controlled by adding techniques and passes.</span></span>

<span data-ttu-id="fd9fc-121">您可以使用其他階段來建立效果，以加速更複雜的轉譯效果。</span><span class="sxs-lookup"><span data-stu-id="fd9fc-121">Effects can be created with additional passes to facilitate more complex rendering effects.</span></span> <span data-ttu-id="fd9fc-122">技術支援任意數目的傳遞：</span><span class="sxs-lookup"><span data-stu-id="fd9fc-122">A technique supports an arbitrary number of passes:</span></span>


```
technique T0
{
    pass P0
    { ... }

    pass P1
    { ... }

    ...

    pass Pn
    { ... }
}
```



<span data-ttu-id="fd9fc-123">也可以使用任意數目的技巧來建立效果。</span><span class="sxs-lookup"><span data-stu-id="fd9fc-123">Effects can also be created with an arbitrary number of techniques.</span></span>


```
technique T0
{
    pass P0
    { ... }
}

technique T1
{
    pass P0
    { ... }

    pass P1
    { ... }
}

...

technique Tn
{
    pass P0
    { ... }
}

technique TVertexShaderOnly
{
    pass P0
    {
        VertexShader =
        asm
        {
         // assembly-language shader code goes here
         ...
        };
    }
}
```



<span data-ttu-id="fd9fc-124">您可以將任何名稱提供給這些技巧和 pass。</span><span class="sxs-lookup"><span data-stu-id="fd9fc-124">The techniques and passes can be given arbitrary names.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd9fc-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="fd9fc-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd9fc-126">影響</span><span class="sxs-lookup"><span data-stu-id="fd9fc-126">Effects</span></span>](effects.md)
</dt> </dl>

 

 




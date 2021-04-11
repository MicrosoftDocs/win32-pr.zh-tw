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
# <a name="organizing-state-in-an-effect-direct3d-10"></a>將效果中的狀態組織 (Direct3D 10) 

使用 Direct3D 10 時，特定管線階段的效果狀態會依照下列結構來組織：



| 管線狀態  | 結構                                                                                                          |
|-----------------|--------------------------------------------------------------------------------------------------------------------|
| 輸入組合器 | [**D3D10 \_ 輸入 \_ 元素 \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)                                                    |
| 光柵   | [**D3D10 轉譯器 \_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)                                                           |
| 輸出合併   | [**D3D10 \_BLEND \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)和 [ **D3D10 \_ 深度 \_ 樣板 \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc) |



 

針對著色器階段，其中的狀態變更數目需要更多應用程式控制，狀態已分割成常數緩衝區狀態、取樣器狀態和著色器資源狀態。 這可讓精心設計的應用程式只更新變更狀態，藉由減少必須傳遞至 GPU 的資料量來改善效能。

那麼，您要如何在效果中組織管線狀態呢？

答案是，順序並不重要。 全域變數不需要位於頂端。 不過，SDK 中的所有範例都遵循相同的順序，因為最好的做法是以相同的方式來組織資料。 這是 DirectX SDK 範例中資料排序的簡短描述。

-   [全域變數](#global-variables)
-   [著色器](#shaders)
-   [技術與通過](#techniques-and-passes)

## <a name="global-variables"></a>全域變數

就像標準 C 實務一樣，全域變數是在檔案頂端先宣告。 最常見的情況是，這些變數會由應用程式初始化，然後用於效果中。 有時候它們會初始化且永遠不會變更，而在其他情況下，則會更新每個畫面格。 如同 C 函式範圍規則，在效果函式範圍外宣告的效果變數在整個效果中都是可見的;只有在該函式內才能看到任何在效果函式內宣告的變數。

以下是在 BasicHLSL10 中宣告的變數範例。


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



效果變數的語法在 [ (Direct3D 10) 的效果變數語法 ](d3d10-effect-variable-syntax.md)中更加詳盡。 效果紋理取樣器的語法在 [取樣器類型 (DIRECTX HLSL) ](../direct3dhlsl/dx-graphics-hlsl-sampler.md)中更詳盡。

## <a name="shaders"></a>著色器

著色器是小型的可執行程式。 您可以將著色器視為封裝著色器狀態，因為 HLSL 程式碼會執行著色器功能。 管線會使用三種不同的著色器。

-   頂點著色器-在頂點資料上操作。 中的一個頂點會產生一個頂點。
-   幾何著色器-操作基本資料。 中的一個基本專案可能會產生0、1或許多基本專案。
-   圖元著色器-在圖元資料上操作。 中的一個圖元會產生1圖元輸出 (除非圖元從轉譯) 挑選出來。

著色器是區域函式，並遵循 C 樣式函數規則。 當編譯效果時，會編譯每個著色器，並在內部儲存每個著色器函式的指標。 編譯成功時，會傳回 ID3D10Effect 介面。 此時，編譯的效果會採用中繼格式。

若要瞭解已編譯著色器的詳細資訊，您將需要使用著色器反映。 這基本上就像是要求執行時間對著色器進行反編譯，然後將資訊傳回給您，以瞭解著色器程式碼。


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



效果著色器的語法在 [ (Direct3D 10) 的效果 ](d3d10-effect-function-syntax.md)函式語法中是更完整的詳細說明。

## <a name="techniques-and-passes"></a>技術與通過

技術是轉譯行程的集合， (至少必須有一個 pass) 。 每個效果傳遞 (在轉譯迴圈中的單一傳遞範圍中類似) 定義著色器狀態和轉譯幾何所需的任何其他管線狀態。

以下是其中一個技巧 (的範例，其中包含 BasicHLSL10 的一個 pass) 。


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



效果著色器的語法更完整地說明 [ (Direct3D 10) 的有效技巧語法 ](d3d10-effect-technique-syntax.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (Direct3D 10) 的效果 ](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 

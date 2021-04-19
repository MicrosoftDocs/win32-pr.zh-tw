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
# <a name="writing-an-effect-direct3d-9"></a>將效果寫入 (Direct3D 9) 

寫入效果需要您瞭解效果語法，並產生必要的狀態資訊。 您可以新增著色器狀態、材質和取樣器狀態，以及您的應用程式在效果中所需的所有管線狀態。

效果語法在 [ (Direct3D 9) 的效果格式 ](dx9-graphics-reference-effects-file-format.md)中有詳細的說明。 效果通常會封裝到效果檔案中， ( fx) 但也可以撰寫為應用程式中的文字字串。

## <a name="effect-example"></a>效果範例

效果包含三種狀態類型：著色器狀態、材質和取樣器狀態，以及管線狀態。 以下是來自 [BasicHLSL 範例](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx)的效果範例：


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



此效果包含：

-   著色器狀態，這是與頂點著色器和圖元著色器相關聯的所有狀態。 這是由頂點和圖元著色器函式、它們所需的任何全域變數及其輸入和輸出資料結構所定義，這些都列在這裡：

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

    

-   材質和取樣器狀態，也就是紋理物件和取樣器物件的全域變數：

    ```
    texture g_MeshTexture;              // Color texture for mesh

    sampler MeshTextureSampler = 
    sampler_state
    {
       ...
    };
    ```

    

-   其他效果狀態。 此範例中未明確使用任何其他效果狀態。 如果有的話，這會是它所套用之傳遞的內部技術：

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

    

## <a name="effects-contain-one-or-more-techniques-and-passes"></a>效果包含一或多個技術與通過

效果轉譯選項是藉由新增技術和傳遞來控制。

您可以使用其他階段來建立效果，以加速更複雜的轉譯效果。 技術支援任意數目的傳遞：


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



也可以使用任意數目的技巧來建立效果。


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



您可以將任何名稱提供給這些技巧和 pass。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[影響](effects.md)
</dt> </dl>

 

 




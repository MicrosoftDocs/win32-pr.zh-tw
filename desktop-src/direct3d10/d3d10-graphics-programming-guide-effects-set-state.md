---
description: 某些效果常數只需要初始化。 請參閱在 Direct3D 10 中設定效果變數的基本程式碼。
ms.assetid: 743261a8-fdd8-492e-be8a-4faeb9b6f986
title: '設定效果狀態 (Direct3D 10) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6df7133276b6392abca8d75eed16de896fb58f84
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404721"
---
# <a name="set-effect-state-direct3d-10"></a>設定效果狀態 (Direct3D 10) 

某些效果常數只需要初始化。 一旦初始化之後，效果狀態就會設定為整個轉譯迴圈的裝置。 每次呼叫轉譯迴圈時，都需要更新其他變數。 以下顯示每個變數類型的設定效果變數的基本程式碼。

效果會封裝完成轉譯階段所需的所有轉譯狀態。 就 API 而言，有三種類型的狀態封裝在效果中。

-   [常數狀態](#constant-state)
-   [著色器狀態](#shader-state)
-   [材質狀態](#texture-state)

## <a name="constant-state"></a>常數狀態

首先，使用 HLSL 資料類型來宣告效果中的變數。


```
//--------------------------------------------------------------------------------------
// Global variables
//--------------------------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
int g_nNumLights;

float3 g_LightDir[3];               // Light's direction in world space
float4 g_LightDiffuse[3];           // Light's diffuse color
float4 g_LightAmbient;              // Light's ambient color

Texture2D g_MeshTexture;            // Color texture for mesh

float    g_fTime;                   // App's time in seconds
float4x4 g_mWorld;                  // World matrix for object
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix
```



其次，在應用程式中宣告可由應用程式設定的變數，然後更新效果變數。


```
           
    D3DXMATRIX  mWorldViewProjection;
    D3DXVECTOR3 vLightDir[MAX_LIGHTS];
    D3DXVECTOR4 vLightDiffuse[MAX_LIGHTS];
    D3DXMATRIX  mWorld;
    D3DXMATRIX  mView;
    D3DXMATRIX  mProj;

    // Get the projection and view matrix from the camera class
    mWorld = g_mCenterMesh * *g_Camera.GetWorldMatrix();
    mProj = *g_Camera.GetProjMatrix();
    mView = *g_Camera.GetViewMatrix();

    
OnD3D10CreateDevice()
{
  ...
    g_pLightDir = g_pEffect10->GetVariableByName( "g_LightDir" )->AsVector();
    g_pLightDiffuse = g_pEffect10->GetVariableByName( "g_LightDiffuse" )->AsVector();
    g_pmWorldViewProjection = g_pEffect10->GetVariableByName( 
        "g_mWorldViewProjection" )->AsMatrix();
    g_pmWorld = g_pEffect10->GetVariableByName( "g_mWorld" )->AsMatrix();
    g_pfTime = g_pEffect10->GetVariableByName( "g_fTime" )->AsScalar();
    g_pMaterialAmbientColor = g_pEffect10->GetVariableByName("g_MaterialAmbientColor")->AsVector();
    g_pMaterialDiffuseColor = g_pEffect10->GetVariableByName( 
        "g_MaterialDiffuseColor" )->AsVector();
    g_pnNumLights = g_pEffect10->GetVariableByName( "g_nNumLights" )->AsScalar();
}
```



第三，使用 update 方法，在效果變數中設定應用程式中的變數值。


```
           
OnD3D10FrameRender()
{
    ...
    g_pLightDir->SetRawValue( vLightDir, 0, sizeof(D3DXVECTOR3)*MAX_LIGHTS );
    g_pLightDiffuse->SetFloatVectorArray( (float*)vLightDiffuse, 0, MAX_LIGHTS );
    g_pmWorldViewProjection->SetMatrix( (float*)&mWorldViewProjection );
    g_pmWorld->SetMatrix( (float*)&mWorld );
    g_pfTime->SetFloat( (float)fTime );
    g_pnNumLights->SetInt( g_nNumActiveLights );
}
```



### <a name="two-ways-to-get-the-state-in-an-effect-variable"></a>有兩種方式可取得效果變數中的狀態

有兩種方式可取得效果變數中包含的狀態。 給定已載入記憶體的效果。

其中一種方式是從已轉換成取樣器介面的 [**ID3D10EffectVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) 取得取樣器狀態。


```
D3D10_SAMPLER_DESC sampler_desc;
ID3D10EffectVariable* l_pD3D10EffectVariable = NULL;
if( g_pEffect10 )
{
    l_pD3D10EffectVariable = g_pEffect10->GetVariableByName( "MeshTextureSampler" );
    if( l_pD3D10EffectVariable )
        hr = (l_pD3D10EffectVariable->AsSampler())->GetBackingStore( 0, 
            &sampler_desc );
}
```



另一種方式是從 [**ID3D10SamplerState 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10samplerstate)取得取樣器狀態。


```
ID3D10SamplerState* l_ppSamplerState = NULL;
D3D10_SAMPLER_DESC sampler_desc;
ID3D10EffectVariable* l_pD3D10EffectVariable = NULL;
if( g_pEffect10 )
{
    l_pD3D10EffectVariable = g_pEffect10->GetVariableByName( "MeshTextureSampler" );
    if( l_pD3D10EffectVariable )
    {
        hr = (l_pD3D10EffectVariable->AsSampler())->GetSampler( 0, 
            &l_ppSamplerState );
        if( l_ppSamplerState )
            l_ppSamplerState->GetDesc( &sampler_desc );
    }
}
```



## <a name="shader-state"></a>著色器狀態

著色器中的著色器狀態是在效果技術中宣告和指派。


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



其運作方式就如同您未使用效果一樣。 有三個呼叫，每一種著色器的類型都 (頂點、幾何和圖元) 。 第一個 SetVertexShader 會呼叫 [**ID3D10Device：： VSSetShader**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader)。 CompileShader 是特殊效果函式，會採用著色器設定檔 (vs \_ 4 \_ 0) ，而頂點著色器函式的名稱 (RenderVS) 。 換句話說，這些 SetXXXShader 呼叫會編譯其相關聯的著色器函式，並將指標傳回至編譯的著色器。

## <a name="texture-state"></a>材質狀態

材質狀態比設定變數稍微複雜一點，因為材質資料不像變數一樣直接讀取，而是從材質進行取樣。 因此，您必須將材質變數 (定義為一般變數，但它會使用材質類型) ，而您必須定義取樣條件。 以下是紋理變數宣告和對應的取樣狀態宣告的範例。


```
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

```



以下是從應用程式設定材質的範例。 在此範例中，材質會儲存在建立效果時所載入的網格資料中。

第一個步驟是從網格) 取得效果 (的材質指標。


```
ID3D10EffectShaderResourceVariable* g_ptxDiffuse = NULL;

    // Obtain variables
    g_ptxDiffuse = g_pEffect10->GetVariableByName( "g_MeshTexture" )->AsShaderResource();
```



第二個步驟是指定用來存取材質的視圖。 此視圖會定義從材質資源存取資料的一般方式。


```
   
OnD3D10FrameRender()
{
  ID3D10ShaderResourceView* pDiffuseRV = NULL;

   ...
   pDiffuseRV = g_Mesh10.GetMaterial(pSubset->MaterialID)->pDiffuseRV10;
   g_ptxDiffuse->SetResource( pDiffuseRV );
   ...
}   
```



如需有關如何查看資源的詳細資訊，請參閱 [ (Direct3D 10) 的材質視圖 ](d3d10-graphics-programming-guide-resources-access-views.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉譯 (Direct3D 10) 的效果 ](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 




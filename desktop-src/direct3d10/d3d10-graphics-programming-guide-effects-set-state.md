---
description: 某些效果常數只需要初始化。
ms.assetid: 743261a8-fdd8-492e-be8a-4faeb9b6f986
title: '設定效果狀態 (Direct3D 10) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f14d4cdfb23c56f9534d1b4029482ce4e494b37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936181"
---
# <a name="set-effect-state-direct3d-10"></a><span data-ttu-id="7b2bb-103">設定效果狀態 (Direct3D 10) </span><span class="sxs-lookup"><span data-stu-id="7b2bb-103">Set Effect State (Direct3D 10)</span></span>

<span data-ttu-id="7b2bb-104">某些效果常數只需要初始化。</span><span class="sxs-lookup"><span data-stu-id="7b2bb-104">Some effect constants only need to be initialized.</span></span> <span data-ttu-id="7b2bb-105">一旦初始化之後，效果狀態就會設定為整個轉譯迴圈的裝置。</span><span class="sxs-lookup"><span data-stu-id="7b2bb-105">Once initialized, the effect state is set to the device for the entire render loop.</span></span> <span data-ttu-id="7b2bb-106">每次呼叫轉譯迴圈時，都需要更新其他變數。</span><span class="sxs-lookup"><span data-stu-id="7b2bb-106">Other variables need to be updated each time the render loop is called.</span></span> <span data-ttu-id="7b2bb-107">以下顯示每個變數類型的設定效果變數的基本程式碼。</span><span class="sxs-lookup"><span data-stu-id="7b2bb-107">The basic code for setting effect variables is shown below, for each of the types of variables.</span></span>

<span data-ttu-id="7b2bb-108">效果會封裝完成轉譯階段所需的所有轉譯狀態。</span><span class="sxs-lookup"><span data-stu-id="7b2bb-108">An effect encapsulates all of the render state required to do a rendering pass.</span></span> <span data-ttu-id="7b2bb-109">就 API 而言，有三種類型的狀態封裝在效果中。</span><span class="sxs-lookup"><span data-stu-id="7b2bb-109">In terms of the API, there are three types of state encapsulated in an effect.</span></span>

-   [<span data-ttu-id="7b2bb-110">常數狀態</span><span class="sxs-lookup"><span data-stu-id="7b2bb-110">Constant State</span></span>](#constant-state)
-   [<span data-ttu-id="7b2bb-111">著色器狀態</span><span class="sxs-lookup"><span data-stu-id="7b2bb-111">Shader State</span></span>](#shader-state)
-   [<span data-ttu-id="7b2bb-112">材質狀態</span><span class="sxs-lookup"><span data-stu-id="7b2bb-112">Texture State</span></span>](#texture-state)

## <a name="constant-state"></a><span data-ttu-id="7b2bb-113">常數狀態</span><span class="sxs-lookup"><span data-stu-id="7b2bb-113">Constant State</span></span>

<span data-ttu-id="7b2bb-114">首先，使用 HLSL 資料類型來宣告效果中的變數。</span><span class="sxs-lookup"><span data-stu-id="7b2bb-114">First, declare variables in an effect using HLSL data types.</span></span>


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



<span data-ttu-id="7b2bb-115">其次，在應用程式中宣告可由應用程式設定的變數，然後更新效果變數。</span><span class="sxs-lookup"><span data-stu-id="7b2bb-115">Second, declare variables in the application that can be set by the application, and will then update the effect variables.</span></span>


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



<span data-ttu-id="7b2bb-116">第三，使用 update 方法，在效果變數中設定應用程式中的變數值。</span><span class="sxs-lookup"><span data-stu-id="7b2bb-116">Third, use the update methods to set the value of the variables in the application in the effect variables.</span></span>


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



### <a name="two-ways-to-get-the-state-in-an-effect-variable"></a><span data-ttu-id="7b2bb-117">有兩種方式可取得效果變數中的狀態</span><span class="sxs-lookup"><span data-stu-id="7b2bb-117">Two Ways to Get the State in an Effect Variable</span></span>

<span data-ttu-id="7b2bb-118">有兩種方式可取得效果變數中包含的狀態。</span><span class="sxs-lookup"><span data-stu-id="7b2bb-118">There are two ways to get the state contained in an effect variable.</span></span> <span data-ttu-id="7b2bb-119">給定已載入記憶體的效果。</span><span class="sxs-lookup"><span data-stu-id="7b2bb-119">Given an effect that has been loaded into memory.</span></span>

<span data-ttu-id="7b2bb-120">其中一種方式是從已轉換成取樣器介面的 [**ID3D10EffectVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) 取得取樣器狀態。</span><span class="sxs-lookup"><span data-stu-id="7b2bb-120">One way is to get the sampler state from an [**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) that has been cast as a sampler interface.</span></span>


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



<span data-ttu-id="7b2bb-121">另一種方式是從 [**ID3D10SamplerState 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10samplerstate)取得取樣器狀態。</span><span class="sxs-lookup"><span data-stu-id="7b2bb-121">The other way is to get the sampler state from an [**ID3D10SamplerState Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10samplerstate).</span></span>


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



## <a name="shader-state"></a><span data-ttu-id="7b2bb-122">著色器狀態</span><span class="sxs-lookup"><span data-stu-id="7b2bb-122">Shader State</span></span>

<span data-ttu-id="7b2bb-123">著色器中的著色器狀態是在效果技術中宣告和指派。</span><span class="sxs-lookup"><span data-stu-id="7b2bb-123">Shader state is declared and assigned in an effect technique, within a pass.</span></span>


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



<span data-ttu-id="7b2bb-124">其運作方式就如同您未使用效果一樣。</span><span class="sxs-lookup"><span data-stu-id="7b2bb-124">This works just like it would if you were not using an effect.</span></span> <span data-ttu-id="7b2bb-125">有三個呼叫，每一種著色器的類型都 (頂點、幾何和圖元) 。</span><span class="sxs-lookup"><span data-stu-id="7b2bb-125">There are three calls, one for each type of shader (vertex, geometry, and pixel).</span></span> <span data-ttu-id="7b2bb-126">第一個 SetVertexShader 會呼叫 [**ID3D10Device：： VSSetShader**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader)。</span><span class="sxs-lookup"><span data-stu-id="7b2bb-126">The first one, SetVertexShader, calls [**ID3D10Device::VSSetShader**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader).</span></span> <span data-ttu-id="7b2bb-127">CompileShader 是特殊效果函式，會採用著色器設定檔 (vs \_ 4 \_ 0) ，而頂點著色器函式的名稱 (RenderVS) 。</span><span class="sxs-lookup"><span data-stu-id="7b2bb-127">CompileShader is a special effect function that takes the shader profile(vs\_4\_0) and the name of the vertex shader function (RenderVS).</span></span> <span data-ttu-id="7b2bb-128">換句話說，這些 SetXXXShader 呼叫會編譯其相關聯的著色器函式，並將指標傳回至編譯的著色器。</span><span class="sxs-lookup"><span data-stu-id="7b2bb-128">In other words, each of these SetXXXShader calls compiles their associated shader function and returns a pointer to the compiled shader.</span></span>

## <a name="texture-state"></a><span data-ttu-id="7b2bb-129">材質狀態</span><span class="sxs-lookup"><span data-stu-id="7b2bb-129">Texture State</span></span>

<span data-ttu-id="7b2bb-130">材質狀態比設定變數稍微複雜一點，因為材質資料不像變數一樣直接讀取，而是從材質進行取樣。</span><span class="sxs-lookup"><span data-stu-id="7b2bb-130">Texture state is a little more complex than setting a variable, because texture data is not simply read like a variable, it is sampled from a texture.</span></span> <span data-ttu-id="7b2bb-131">因此，您必須將材質變數 (定義為一般變數，但它會使用材質類型) ，而您必須定義取樣條件。</span><span class="sxs-lookup"><span data-stu-id="7b2bb-131">Therefore, you must define the texture variable (just like a normal variable except it uses a texture type) and you must define the sampling conditions.</span></span> <span data-ttu-id="7b2bb-132">以下是紋理變數宣告和對應的取樣狀態宣告的範例。</span><span class="sxs-lookup"><span data-stu-id="7b2bb-132">Here is an example of a texture variable declaration and the corresponding sampling state declaration.</span></span>


```
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

```



<span data-ttu-id="7b2bb-133">以下是從應用程式設定材質的範例。</span><span class="sxs-lookup"><span data-stu-id="7b2bb-133">Here is an example of setting a texture from an application.</span></span> <span data-ttu-id="7b2bb-134">在此範例中，材質會儲存在建立效果時所載入的網格資料中。</span><span class="sxs-lookup"><span data-stu-id="7b2bb-134">In this example, the texture is stored in the mesh data, that was loaded when the effect was created.</span></span>

<span data-ttu-id="7b2bb-135">第一個步驟是從網格) 取得效果 (的材質指標。</span><span class="sxs-lookup"><span data-stu-id="7b2bb-135">The first step is getting a pointer to the texture from the effect (from the mesh).</span></span>


```
ID3D10EffectShaderResourceVariable* g_ptxDiffuse = NULL;

    // Obtain variables
    g_ptxDiffuse = g_pEffect10->GetVariableByName( "g_MeshTexture" )->AsShaderResource();
```



<span data-ttu-id="7b2bb-136">第二個步驟是指定用來存取材質的視圖。</span><span class="sxs-lookup"><span data-stu-id="7b2bb-136">The second step is specifying a view for accessing the texture.</span></span> <span data-ttu-id="7b2bb-137">此視圖會定義從材質資源存取資料的一般方式。</span><span class="sxs-lookup"><span data-stu-id="7b2bb-137">The view defines a general way to access the data from the texture resource.</span></span>


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



<span data-ttu-id="7b2bb-138">如需有關如何查看資源的詳細資訊，請參閱 [ (Direct3D 10) 的材質視圖 ](d3d10-graphics-programming-guide-resources-access-views.md)。</span><span class="sxs-lookup"><span data-stu-id="7b2bb-138">For more information about viewing resources, see [Texture Views (Direct3D 10)](d3d10-graphics-programming-guide-resources-access-views.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b2bb-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="7b2bb-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b2bb-140">轉譯 (Direct3D 10) 的效果 </span><span class="sxs-lookup"><span data-stu-id="7b2bb-140">Rendering an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 




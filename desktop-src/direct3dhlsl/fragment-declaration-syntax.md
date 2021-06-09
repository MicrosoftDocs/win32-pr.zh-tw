---
title: " (Direct3D 9 HLSL) 的片段宣告語法"
description: 您可以透過新增片段宣告，將每個 Microsoft 高階著色器語言 (HLSL) 函數轉換成著色器片段。
ms.assetid: 34ceef8c-8fb9-4c73-86cc-014b7a2ee4d7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 60ac1153ff3491bc904f4f759f6653cb4243adff
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825725"
---
# <a name="fragment-declaration-syntax-direct3d-9-hlsl"></a><span data-ttu-id="aa894-103"> (Direct3D 9 HLSL) 的片段宣告語法</span><span class="sxs-lookup"><span data-stu-id="aa894-103">Fragment Declaration Syntax (Direct3D 9 HLSL)</span></span>

<span data-ttu-id="aa894-104">您可以透過新增片段宣告，將每個 Microsoft 高階著色器語言 (HLSL) 函數轉換成著色器片段。</span><span class="sxs-lookup"><span data-stu-id="aa894-104">Each Microsoft High Level Shader Language (HLSL) function can be converted into a shader fragment with the addition of a fragment declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa894-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa894-105">Syntax</span></span>


```
fragmentKeyword FragmentName = compile_fragment shaderProfile FunctionName();
```



<span data-ttu-id="aa894-106">其中：</span><span class="sxs-lookup"><span data-stu-id="aa894-106">where:</span></span>



| <span data-ttu-id="aa894-107">值</span><span class="sxs-lookup"><span data-stu-id="aa894-107">Value</span></span>                  | <span data-ttu-id="aa894-108">描述</span><span class="sxs-lookup"><span data-stu-id="aa894-108">Description</span></span>                                                                                                                                                                                                                                                      |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa894-109">fragmentKeyword</span><span class="sxs-lookup"><span data-stu-id="aa894-109">fragmentKeyword</span></span>   | <span data-ttu-id="aa894-110">必要關鍵字。</span><span class="sxs-lookup"><span data-stu-id="aa894-110">Required keyword.</span></span> <span data-ttu-id="aa894-111">可能是 pixelfragment 或 vertexfragment。</span><span class="sxs-lookup"><span data-stu-id="aa894-111">Either pixelfragment or vertexfragment.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="aa894-112">FragmentName</span><span class="sxs-lookup"><span data-stu-id="aa894-112">FragmentName</span></span>      | <span data-ttu-id="aa894-113">指定已編譯片段名稱的 ASCII 文字字串。</span><span class="sxs-lookup"><span data-stu-id="aa894-113">An ASCII text string that specifies the compiled fragment name.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="aa894-114">編譯 \_ 片段</span><span class="sxs-lookup"><span data-stu-id="aa894-114">compile\_fragment</span></span> | <span data-ttu-id="aa894-115">必要關鍵字。</span><span class="sxs-lookup"><span data-stu-id="aa894-115">Required keyword.</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="aa894-116">shaderProfile</span><span class="sxs-lookup"><span data-stu-id="aa894-116">shaderProfile</span></span>     | <span data-ttu-id="aa894-117">要針對編譯的著色器模型。</span><span class="sxs-lookup"><span data-stu-id="aa894-117">The shader model to compile against.</span></span> <span data-ttu-id="aa894-118">任何有效的頂點著色器設定檔 (查看 [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) 或圖元著色器設定檔 (參閱 [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)) 。</span><span class="sxs-lookup"><span data-stu-id="aa894-118">Any valid vertex shader profile (see [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) or pixel shader profile (see [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)).</span></span> |
| <span data-ttu-id="aa894-119">FunctionName () </span><span class="sxs-lookup"><span data-stu-id="aa894-119">FunctionName()</span></span>    | <span data-ttu-id="aa894-120">著色器函式名稱，後面接著括弧。</span><span class="sxs-lookup"><span data-stu-id="aa894-120">The shader function name, followed by parentheses.</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="aa894-121">共用片段參數會藉由將 ' r \_ ' 前置詞新增至其語義來標記。</span><span class="sxs-lookup"><span data-stu-id="aa894-121">Shared fragment parameters are marked by adding an 'r\_' prefix to their semantic.</span></span>


```
void AmbientDiffuse( float3 vPosWorld: r_PosWorld,
                     float3 vNormalWorld: r_NormalWorld,
                     out float4 vColor: COLOR0 )
{  
    // Compute the light vector
    float3 vLight = normalize( g_vLightPosition - vPosWorld );
    
    // Compute the ambient and diffuse components of illumination
    vColor = g_vLightColor * g_vMaterialAmbient;
    vColor += g_vLightColor * g_vMaterialDiffuse * saturate( dot( vLight, vNormalWorld ) );
}
vertexfragment AmbientDiffuseFragment = compile_fragment vs_1_1 AmbientDiffuse();
```



<span data-ttu-id="aa894-122">在此範例中，r \_ PosWorld 和 r \_ NormalWorld 語義會識別這兩個參數是其他片段之間的共用參數。</span><span class="sxs-lookup"><span data-stu-id="aa894-122">In this example, the r\_PosWorld and r\_NormalWorld semantics identify that these two parameters are shared parameters among other fragments.</span></span>

> [!Note]  
> <span data-ttu-id="aa894-123">片段連結器是 D3DX 9 中的 Microsoft Direct3D 9 技術。</span><span class="sxs-lookup"><span data-stu-id="aa894-123">Fragment linker was a Microsoft Direct3D 9 technology in D3DX 9.</span></span> <span data-ttu-id="aa894-124">片段連結器是一種工具 (Flink.exe) 、D3DX 9 API，以及 HLSL 增強功能。</span><span class="sxs-lookup"><span data-stu-id="aa894-124">Fragment linker was a tool (Flink.exe), a D3DX 9 API, and an HLSL enhancement.</span></span> <span data-ttu-id="aa894-125">從2009年8月的 DirectX SDK 版本中卸載了片段連結器。</span><span class="sxs-lookup"><span data-stu-id="aa894-125">Fragment linker was dropped as of the August 2009 DirectX SDK release.</span></span> <span data-ttu-id="aa894-126">片段連結器從未套用到 Microsoft Direct3D 10、Microsoft Direct3D 10.1 或 Microsoft Direct3D 11。</span><span class="sxs-lookup"><span data-stu-id="aa894-126">Fragment linker never applied to Microsoft Direct3D 10, Microsoft Direct3D 10.1, or Microsoft Direct3D 11.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="aa894-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="aa894-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa894-128">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="aa894-128">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 

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
ms.openlocfilehash: 98e609820e67cc3ede6c3e280f63513850fed364
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023668"
---
# <a name="fragment-declaration-syntax-direct3d-9-hlsl"></a><span data-ttu-id="3917e-103"> (Direct3D 9 HLSL) 的片段宣告語法</span><span class="sxs-lookup"><span data-stu-id="3917e-103">Fragment Declaration Syntax (Direct3D 9 HLSL)</span></span>

<span data-ttu-id="3917e-104">您可以透過新增片段宣告，將每個 Microsoft 高階著色器語言 (HLSL) 函數轉換成著色器片段。</span><span class="sxs-lookup"><span data-stu-id="3917e-104">Each Microsoft High Level Shader Language (HLSL) function can be converted into a shader fragment with the addition of a fragment declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="3917e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3917e-105">Syntax</span></span>


```
fragmentKeyword FragmentName = compile_fragment shaderProfile FunctionName();
```



<span data-ttu-id="3917e-106">其中：</span><span class="sxs-lookup"><span data-stu-id="3917e-106">where:</span></span>



|                   |                                                                                                                                                                                                                                                       |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3917e-107">fragmentKeyword</span><span class="sxs-lookup"><span data-stu-id="3917e-107">fragmentKeyword</span></span>   | <span data-ttu-id="3917e-108">必要關鍵字。</span><span class="sxs-lookup"><span data-stu-id="3917e-108">Required keyword.</span></span> <span data-ttu-id="3917e-109">可能是 pixelfragment 或 vertexfragment。</span><span class="sxs-lookup"><span data-stu-id="3917e-109">Either pixelfragment or vertexfragment.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="3917e-110">FragmentName</span><span class="sxs-lookup"><span data-stu-id="3917e-110">FragmentName</span></span>      | <span data-ttu-id="3917e-111">指定已編譯片段名稱的 ASCII 文字字串。</span><span class="sxs-lookup"><span data-stu-id="3917e-111">An ASCII text string that specifies the compiled fragment name.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="3917e-112">編譯 \_ 片段</span><span class="sxs-lookup"><span data-stu-id="3917e-112">compile\_fragment</span></span> | <span data-ttu-id="3917e-113">必要關鍵字。</span><span class="sxs-lookup"><span data-stu-id="3917e-113">Required keyword.</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="3917e-114">shaderProfile</span><span class="sxs-lookup"><span data-stu-id="3917e-114">shaderProfile</span></span>     | <span data-ttu-id="3917e-115">要針對編譯的著色器模型。</span><span class="sxs-lookup"><span data-stu-id="3917e-115">The shader model to compile against.</span></span> <span data-ttu-id="3917e-116">任何有效的頂點著色器設定檔 (查看 [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) 或圖元著色器設定檔 (參閱 [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)) 。</span><span class="sxs-lookup"><span data-stu-id="3917e-116">Any valid vertex shader profile (see [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) or pixel shader profile (see [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)).</span></span> |
| <span data-ttu-id="3917e-117">FunctionName () </span><span class="sxs-lookup"><span data-stu-id="3917e-117">FunctionName()</span></span>    | <span data-ttu-id="3917e-118">著色器函式名稱，後面接著括弧。</span><span class="sxs-lookup"><span data-stu-id="3917e-118">The shader function name, followed by parentheses.</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="3917e-119">共用片段參數會藉由將 ' r \_ ' 前置詞新增至其語義來標記。</span><span class="sxs-lookup"><span data-stu-id="3917e-119">Shared fragment parameters are marked by adding an 'r\_' prefix to their semantic.</span></span>


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



<span data-ttu-id="3917e-120">在此範例中，r \_ PosWorld 和 r \_ NormalWorld 語義會識別這兩個參數是其他片段之間的共用參數。</span><span class="sxs-lookup"><span data-stu-id="3917e-120">In this example, the r\_PosWorld and r\_NormalWorld semantics identify that these two parameters are shared parameters among other fragments.</span></span>

> [!Note]  
> <span data-ttu-id="3917e-121">片段連結器是 D3DX 9 中的 Microsoft Direct3D 9 技術。</span><span class="sxs-lookup"><span data-stu-id="3917e-121">Fragment linker was a Microsoft Direct3D 9 technology in D3DX 9.</span></span> <span data-ttu-id="3917e-122">片段連結器是一種工具 (Flink.exe) 、D3DX 9 API，以及 HLSL 增強功能。</span><span class="sxs-lookup"><span data-stu-id="3917e-122">Fragment linker was a tool (Flink.exe), a D3DX 9 API, and an HLSL enhancement.</span></span> <span data-ttu-id="3917e-123">從2009年8月的 DirectX SDK 版本中卸載了片段連結器。</span><span class="sxs-lookup"><span data-stu-id="3917e-123">Fragment linker was dropped as of the August 2009 DirectX SDK release.</span></span> <span data-ttu-id="3917e-124">片段連結器從未套用到 Microsoft Direct3D 10、Microsoft Direct3D 10.1 或 Microsoft Direct3D 11。</span><span class="sxs-lookup"><span data-stu-id="3917e-124">Fragment linker never applied to Microsoft Direct3D 10, Microsoft Direct3D 10.1, or Microsoft Direct3D 11.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="3917e-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="3917e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3917e-126">著色器模型 3 (DirectX HLSL) </span><span class="sxs-lookup"><span data-stu-id="3917e-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 
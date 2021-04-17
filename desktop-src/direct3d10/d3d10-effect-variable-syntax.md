---
description: 效果變數是使用下列語法來宣告。
ms.assetid: 53939c65-3725-44cc-bec6-775c3b921770
title: " (Direct3D 10) 的效果變數語法"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8068571ff393e83ba0ae11eb2f9cb62f0bbb49df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385945"
---
# <a name="effect-variable-syntax-direct3d-10"></a><span data-ttu-id="997aa-103"> (Direct3D 10) 的效果變數語法</span><span class="sxs-lookup"><span data-stu-id="997aa-103">Effect Variable Syntax (Direct3D 10)</span></span>

<span data-ttu-id="997aa-104">效果變數是使用下列語法來宣告。</span><span class="sxs-lookup"><span data-stu-id="997aa-104">An effect variable is declared with the following syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="997aa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="997aa-105">Syntax</span></span>

<span data-ttu-id="997aa-106">*DataType* *VariableName* \[ ： *SemanticName* \]  <  *注釋*>;</span><span class="sxs-lookup"><span data-stu-id="997aa-106">*DataType* *VariableName* \[ : *SemanticName* \] < *Annotations* >;</span></span>



| <span data-ttu-id="997aa-107">Name</span><span class="sxs-lookup"><span data-stu-id="997aa-107">Name</span></span>         | <span data-ttu-id="997aa-108">描述</span><span class="sxs-lookup"><span data-stu-id="997aa-108">Description</span></span>                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="997aa-109">DataType</span><span class="sxs-lookup"><span data-stu-id="997aa-109">DataType</span></span>     | <span data-ttu-id="997aa-110">任何 [基本](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md) 或 [紋理](../direct3dhlsl/dx-graphics-hlsl-to-type.md) 類型。</span><span class="sxs-lookup"><span data-stu-id="997aa-110">Any [basic](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md) or [texture](../direct3dhlsl/dx-graphics-hlsl-to-type.md) type.</span></span>                                                                        |
| <span data-ttu-id="997aa-111">VariableName</span><span class="sxs-lookup"><span data-stu-id="997aa-111">VariableName</span></span> | <span data-ttu-id="997aa-112">可唯一識別效果變數名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="997aa-112">An ASCII string that uniquely identifies the name of the effect variable.</span></span>                                                                                                                   |
| <span data-ttu-id="997aa-113">SemanticName</span><span class="sxs-lookup"><span data-stu-id="997aa-113">SemanticName</span></span> | <span data-ttu-id="997aa-114">表示應該如何使用變數之其他資訊的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="997aa-114">A ASCII string that denotes additional information about how a variable should be used.</span></span> <span data-ttu-id="997aa-115">語義是 ASCII 字串，可以是預先定義的系統值或自訂使用者字串。</span><span class="sxs-lookup"><span data-stu-id="997aa-115">A semantic is an ASCII string that can be either a predefined system-value or a custom-user string.</span></span> |
| <span data-ttu-id="997aa-116">註解</span><span class="sxs-lookup"><span data-stu-id="997aa-116">Annotations</span></span>  | <span data-ttu-id="997aa-117"> (中繼資料) 的一或多個使用者提供的資訊，會被效果系統忽略。</span><span class="sxs-lookup"><span data-stu-id="997aa-117">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="997aa-118">如需語法，請參閱 [ (Direct3D 10) 的批註語法 ](d3d10-effect-annotation-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="997aa-118">For syntax, see [Annotation Syntax (Direct3D 10)](d3d10-effect-annotation-syntax.md).</span></span>     |



 

<span data-ttu-id="997aa-119">在所有函式之外宣告的效果變數都會被視為範圍中的全域。在函式中宣告的變數是該函式的本機變數。</span><span class="sxs-lookup"><span data-stu-id="997aa-119">An effect variable that is declared outside of all functions, is considered global in scope; variables declared within a function are local to that function.</span></span>

## <a name="example"></a><span data-ttu-id="997aa-120">範例</span><span class="sxs-lookup"><span data-stu-id="997aa-120">Example</span></span>

<span data-ttu-id="997aa-121">[BasicHLSL10 範例](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)會使用全域變數，而不使用材質色彩、淺色屬性和轉換矩陣的語法。</span><span class="sxs-lookup"><span data-stu-id="997aa-121">The [BasicHLSL10 sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) uses global variables without semantics for material colors, light properties and transformation matrices.</span></span>

<span data-ttu-id="997aa-122">此範例說明全域效果變數。</span><span class="sxs-lookup"><span data-stu-id="997aa-122">This example illustrates global effect variables.</span></span>


```
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
float3 g_LightDir[3];               // Light's direction in world space
float4x4 g_mWorld;                  // World matrix for object
```



<span data-ttu-id="997aa-123">此範例說明著色器函式本機的效果變數。</span><span class="sxs-lookup"><span data-stu-id="997aa-123">This example illustrates effect variables that are local to a shader function.</span></span>


```
VS_OUTPUT RenderSceneVS( ... )
{
    float3 vNormalWorldSpace;
    float4 vAnimatedPos;

    // shader body
}
```



<span data-ttu-id="997aa-124">此範例說明具有語義的函數參數。</span><span class="sxs-lookup"><span data-stu-id="997aa-124">This example illustrates function parameters that have semantics.</span></span>


```
VS_OUTPUT RenderSceneVS( float4 vPos : SV_POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
  ...
}
```



<span data-ttu-id="997aa-125">此範例說明如何宣告材質變數。</span><span class="sxs-lookup"><span data-stu-id="997aa-125">This example illustrates declaring a texture variable.</span></span>


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



<span data-ttu-id="997aa-126">使用紋理取樣器來取樣紋理。</span><span class="sxs-lookup"><span data-stu-id="997aa-126">Sampling a texture is done with a texture sampler.</span></span> <span data-ttu-id="997aa-127">若要設定效果中的取樣器，請參閱 [取樣器類型](../direct3dhlsl/dx-graphics-hlsl-sampler.md)。</span><span class="sxs-lookup"><span data-stu-id="997aa-127">To set up a sampler in an effect, see the [sampler type](../direct3dhlsl/dx-graphics-hlsl-sampler.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="997aa-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="997aa-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="997aa-129">效果格式</span><span class="sxs-lookup"><span data-stu-id="997aa-129">Effect Format</span></span>](d3d10-effect-format.md)
</dt> </dl>

 

 

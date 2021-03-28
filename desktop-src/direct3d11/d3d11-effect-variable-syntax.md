---
title: " (Direct3D 11) 的效果變數語法"
description: 效果變數是利用本節所述的語法來宣告。
ms.assetid: c0cfc9dd-2df3-4f38-a0e4-2e494456b3c9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67710642060ffea642434ba2d23a77cec2fb8bc3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463177"
---
# <a name="effect-variable-syntax-direct3d-11"></a><span data-ttu-id="dac69-103"> (Direct3D 11) 的效果變數語法</span><span class="sxs-lookup"><span data-stu-id="dac69-103">Effect Variable Syntax (Direct3D 11)</span></span>

<span data-ttu-id="dac69-104">效果變數是利用本節所述的語法來宣告。</span><span class="sxs-lookup"><span data-stu-id="dac69-104">An effect variable is declared with the syntax described in this section.</span></span>

## <a name="syntax"></a><span data-ttu-id="dac69-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dac69-105">Syntax</span></span>

<span data-ttu-id="dac69-106">基本語法：</span><span class="sxs-lookup"><span data-stu-id="dac69-106">Basic syntax:</span></span>

<span data-ttu-id="dac69-107">*DataType* *VariableName* \[ *： SemanticName* \]  <  *附注*  >  \[ = InitialValue \] ;</span><span class="sxs-lookup"><span data-stu-id="dac69-107">*DataType* *VariableName* \[ *: SemanticName* \] < *Annotations* > \[ = InitialValue \];</span></span>

<span data-ttu-id="dac69-108">如需完整語法，請參閱 [ (DIRECTX HLSL) 的變數語法 ](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax) 。</span><span class="sxs-lookup"><span data-stu-id="dac69-108">See [Variable Syntax (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax) for full syntax.</span></span>



| <span data-ttu-id="dac69-109">Name</span><span class="sxs-lookup"><span data-stu-id="dac69-109">Name</span></span>         | <span data-ttu-id="dac69-110">描述</span><span class="sxs-lookup"><span data-stu-id="dac69-110">Description</span></span>                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dac69-111">DataType</span><span class="sxs-lookup"><span data-stu-id="dac69-111">DataType</span></span>     | <span data-ttu-id="dac69-112">任何 [基本](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)、 [材質](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-type)、未排序的存取視圖、著色器或狀態欄塊類型。</span><span class="sxs-lookup"><span data-stu-id="dac69-112">Any [basic](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax), [texture](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-type), unordered access view, shader or state block type.</span></span>                            |
| <span data-ttu-id="dac69-113">VariableName</span><span class="sxs-lookup"><span data-stu-id="dac69-113">VariableName</span></span> | <span data-ttu-id="dac69-114">可唯一識別效果變數名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="dac69-114">An ASCII string that uniquely identifies the name of the effect variable.</span></span>                                                                                                                   |
| <span data-ttu-id="dac69-115">SemanticName</span><span class="sxs-lookup"><span data-stu-id="dac69-115">SemanticName</span></span> | <span data-ttu-id="dac69-116">表示應該如何使用變數之其他資訊的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="dac69-116">A ASCII string that denotes additional information about how a variable should be used.</span></span> <span data-ttu-id="dac69-117">語義是 ASCII 字串，可以是預先定義的系統值或自訂使用者字串。</span><span class="sxs-lookup"><span data-stu-id="dac69-117">A semantic is an ASCII string that can be either a predefined system-value or a custom-user string.</span></span> |
| <span data-ttu-id="dac69-118">註解</span><span class="sxs-lookup"><span data-stu-id="dac69-118">Annotations</span></span>  | <span data-ttu-id="dac69-119"> (中繼資料) 的一或多個使用者提供的資訊，會被效果系統忽略。</span><span class="sxs-lookup"><span data-stu-id="dac69-119">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="dac69-120">如需語法，請參閱 [ (Direct3D 11) 的批註語法 ](d3d11-effect-annotation-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="dac69-120">For syntax, see [Annotation Syntax (Direct3D 11)](d3d11-effect-annotation-syntax.md).</span></span>     |
| <span data-ttu-id="dac69-121">InitialValue</span><span class="sxs-lookup"><span data-stu-id="dac69-121">InitialValue</span></span> | <span data-ttu-id="dac69-122">變數的預設值。</span><span class="sxs-lookup"><span data-stu-id="dac69-122">The default value of the variable.</span></span>                                                                                                                                                          |



 

<span data-ttu-id="dac69-123">在所有函式之外宣告的效果變數都會被視為範圍中的全域。在函式中宣告的變數是該函式的本機變數。</span><span class="sxs-lookup"><span data-stu-id="dac69-123">An effect variable that is declared outside of all functions, is considered global in scope; variables declared within a function are local to that function.</span></span>

## <a name="example"></a><span data-ttu-id="dac69-124">範例</span><span class="sxs-lookup"><span data-stu-id="dac69-124">Example</span></span>

<span data-ttu-id="dac69-125">此範例說明全域效果的數值變數。</span><span class="sxs-lookup"><span data-stu-id="dac69-125">This example illustrates global effect numeric variables.</span></span>


```
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
float3 g_LightDir[3];               // Light's direction in world space
float4x4 g_mWorld;                  // World matrix for object
```



<span data-ttu-id="dac69-126">此範例說明著色器函式本機的效果變數。</span><span class="sxs-lookup"><span data-stu-id="dac69-126">This example illustrates effect variables that are local to a shader function.</span></span>


```
VS_OUTPUT RenderSceneVS( ... )
{
    float3 vNormalWorldSpace;
    float4 vAnimatedPos;

    // shader body
}
```



<span data-ttu-id="dac69-127">此範例說明具有語義的函數參數。</span><span class="sxs-lookup"><span data-stu-id="dac69-127">This example illustrates function parameters that have semantics.</span></span>


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



<span data-ttu-id="dac69-128">此範例說明如何宣告全域材質變數。</span><span class="sxs-lookup"><span data-stu-id="dac69-128">This example illustrates declaring a global texture variable.</span></span>


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



<span data-ttu-id="dac69-129">使用紋理取樣器來取樣紋理。</span><span class="sxs-lookup"><span data-stu-id="dac69-129">Sampling a texture is done with a texture sampler.</span></span> <span data-ttu-id="dac69-130">若要設定效果中的取樣器，請參閱 [取樣器類型](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler)。</span><span class="sxs-lookup"><span data-stu-id="dac69-130">To set up a sampler in an effect, see the [sampler type](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).</span></span>

<span data-ttu-id="dac69-131">此範例說明如何宣告全域未排序的存取視圖變數。</span><span class="sxs-lookup"><span data-stu-id="dac69-131">This example illustrates declaring global unordered access view variables.</span></span>


```
RWStructuredBuffer<uint> bc : register(u2) < string name="bc"; >;
RWBuffer<uint> bRW;
struct S
{
   uint key;
   uint value;
};
AppendStructuredBuffer<S> asb : register(u5);
RWByteAddressBuffer rwbab : register(u1);
RWStructuredBuffer<uint> rwsb : register(u3);
RWTexture1D<float> rwt1d : register(u1);
RWTexture1DArray<uint> rwt1da : register(u4);
RWTexture2D<uint> rwt2d : register(u2);
RWTexture2DArray<uint> rwt2da : register(u6);
RWTexture3D<uint> rwt3d : register(u7); 
 This example illustrates declaring global shader variables.
VertexShader pVS = CompileShader( vs_5_0, VS() );
HullShader pHS = NULL;
DomainShader pDS = NULL;
GeometryShader pGS = ConstructGSWithSO( CompileShader( gs_5_0, VS() ), 
                                        "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                        "3:Texcoord.xyzw; 3:$SKIP.x;", 
                                        NULL, 
                                        NULL, 
                                        1 );
PixelShader pPS = NULL;
ComputeShader pCS = NULL;
This example illustrates declaring global state block variables.
BlendState myBS[2] < bool IsValid = true; >
{
  {
    BlendEnable[0] = false;
  },
  {
    BlendEnable[0] = true;
    SrcBlendAlpha[0] = Inv_Src_Alpha;
  }
};

RasterizerState myRS
{
      FillMode = Solid;
      CullMode = NONE;
      MultisampleEnable = true;
      DepthClipEnable = false;
};

DepthStencilState myDS
{
    DepthEnable = false;
    DepthWriteMask = Zero;
    DepthFunc = Less;
};
sampler mySS[2] : register(s3) 
{
    {
        Filter = ANISOTROPIC;
        MaxAnisotropy = 3;
    },
    {
        Filter = ANISOTROPIC;
        MaxAnisotropy = 4;
    }
};
  
  
```



## <a name="related-topics"></a><span data-ttu-id="dac69-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="dac69-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dac69-133">效果格式</span><span class="sxs-lookup"><span data-stu-id="dac69-133">Effect Format</span></span>](d3d11-effect-format.md)
</dt> </dl>

 

 
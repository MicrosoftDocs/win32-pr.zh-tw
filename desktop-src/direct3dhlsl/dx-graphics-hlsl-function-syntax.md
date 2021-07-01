---
title: 函式宣告語法
description: HLSL 函式會使用下列語法來宣告。
ms.assetid: f8968de2-7b2d-4a2e-8312-cec5b652f700
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 847194c08b865542cff1deb20c8518a7e4b62ab9
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119043"
---
# <a name="function-declaration-syntax"></a><span data-ttu-id="9d0cc-103">函式宣告語法</span><span class="sxs-lookup"><span data-stu-id="9d0cc-103">Function Declaration Syntax</span></span>

<span data-ttu-id="9d0cc-104">HLSL 函式會使用下列語法來宣告。</span><span class="sxs-lookup"><span data-stu-id="9d0cc-104">HLSL functions are declared with the following syntax.</span></span>

<span data-ttu-id="9d0cc-105">\[*StorageClass* \]\[clipplanes () \] \[精確的傳回 \] \_ 值 *名稱* ( \[ *ArgumentList* \] ) \[ ：*語義* \] { \[ *StatementBlock* \] };</span><span class="sxs-lookup"><span data-stu-id="9d0cc-105">\[*StorageClass*\] \[clipplanes()\] \[precise\] Return\_Value *Name* ( \[*ArgumentList*\] ) \[: *Semantic*\] {   \[*StatementBlock*\] };</span></span>



 

## <a name="parameters"></a><span data-ttu-id="9d0cc-106">參數</span><span class="sxs-lookup"><span data-stu-id="9d0cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d0cc-107"><span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*StorageClass*</span><span class="sxs-lookup"><span data-stu-id="9d0cc-107"><span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*StorageClass*</span></span>
</dt> <dd>

<span data-ttu-id="9d0cc-108">重新定義函式宣告的修飾詞。</span><span class="sxs-lookup"><span data-stu-id="9d0cc-108">Modifier that redefines a function declaration.</span></span> <span data-ttu-id="9d0cc-109">**內嵌** 是目前唯一的修飾詞值。</span><span class="sxs-lookup"><span data-stu-id="9d0cc-109">**inline** is currently the only modifier value.</span></span> <span data-ttu-id="9d0cc-110">修飾詞值必須是 **內嵌** 的，因為它也是預設值。</span><span class="sxs-lookup"><span data-stu-id="9d0cc-110">The modifier value must be **inline** because it is also the default value.</span></span> <span data-ttu-id="9d0cc-111">因此，不論您是否指定 **inline**，函式都會內嵌，而 HLSL 中的所有函式都是內嵌的。</span><span class="sxs-lookup"><span data-stu-id="9d0cc-111">Therefore, a function is inline regardless of whether you specify **inline**, and all functions in HLSL are inline.</span></span> <span data-ttu-id="9d0cc-112">內嵌函式會在編譯每個函式呼叫的) 時，產生函數主體的複本 (。</span><span class="sxs-lookup"><span data-stu-id="9d0cc-112">An inline function generates a copy of the function body (when compiling) for each function call.</span></span> <span data-ttu-id="9d0cc-113">這樣做的目的是要降低呼叫函式的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="9d0cc-113">This is done to decrease the overhead of calling the function.</span></span>

</dd> <dt>

<span data-ttu-id="9d0cc-114"><span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplanes*</span><span class="sxs-lookup"><span data-stu-id="9d0cc-114"><span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplanes*</span></span>
</dt> <dd>

<span data-ttu-id="9d0cc-115">選擇性的剪輯平面清單，最多可有6個使用者指定的剪輯平面。</span><span class="sxs-lookup"><span data-stu-id="9d0cc-115">Optional list of clip planes, which is up to 6 user-specified clip planes.</span></span> <span data-ttu-id="9d0cc-116">這是在[功能層級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)9 x 和更高版本上運作的[SV \_ ClipDistance](dx-graphics-hlsl-semantics.md)替代機制 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9d0cc-116">This is an alternate mechanism for [SV\_ClipDistance](dx-graphics-hlsl-semantics.md) that works on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span>

</dd> <dt>

<span data-ttu-id="9d0cc-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*名字*</span><span class="sxs-lookup"><span data-stu-id="9d0cc-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="9d0cc-118">能唯一識別著色器函式名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="9d0cc-118">An ASCII string that uniquely identifies the name of the shader function.</span></span>

</dd> <dt>

<span data-ttu-id="9d0cc-119"><span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*ArgumentList*</span><span class="sxs-lookup"><span data-stu-id="9d0cc-119"><span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*ArgumentList*</span></span>
</dt> <dd>

<span data-ttu-id="9d0cc-120">選擇性引數清單，此清單是傳遞至函式的 [引數](dx-graphics-hlsl-function-parameters.md) 清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="9d0cc-120">Optional argument list, which is a comma-separated list of [arguments](dx-graphics-hlsl-function-parameters.md) passed into a function.</span></span>

</dd> <dt>

<span data-ttu-id="9d0cc-121"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*語義*</span><span class="sxs-lookup"><span data-stu-id="9d0cc-121"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantic*</span></span>
</dt> <dd>

<span data-ttu-id="9d0cc-122">選擇性字串，可識別傳回資料的預期使用方式 (請參閱 [ (DIRECTX HLSL) ](dx-graphics-hlsl-semantics.md)) 的語義。</span><span class="sxs-lookup"><span data-stu-id="9d0cc-122">Optional string that identifies the intended usage of the return data (see [Semantics (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).</span></span>

</dd> <dt>

<span data-ttu-id="9d0cc-123"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span><span class="sxs-lookup"><span data-stu-id="9d0cc-123"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span></span>
</dt> <dd>

<span data-ttu-id="9d0cc-124">組成函數主體的選擇性 [語句](dx-graphics-hlsl-statement-blocks.md) 。</span><span class="sxs-lookup"><span data-stu-id="9d0cc-124">Optional [statements](dx-graphics-hlsl-statement-blocks.md) that make up the body of the function.</span></span> <span data-ttu-id="9d0cc-125">未定義主體的函式稱為函式原型。原型函式的主體必須定義在可呼叫函式之前的其他地方。</span><span class="sxs-lookup"><span data-stu-id="9d0cc-125">A function defined without a body is called a function prototype; the body of a prototype function must be defined elsewhere before the function can be called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d0cc-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="9d0cc-126">Return Value</span></span>

<span data-ttu-id="9d0cc-127">傳回型別可以是下列其中一種 [HLSL 類型](dx-graphics-hlsl-data-types.md)。</span><span class="sxs-lookup"><span data-stu-id="9d0cc-127">The return type can be any one of these [HLSL types](dx-graphics-hlsl-data-types.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9d0cc-128">備註</span><span class="sxs-lookup"><span data-stu-id="9d0cc-128">Remarks</span></span>

<span data-ttu-id="9d0cc-129">此頁面上的語法幾乎描述每種類型的 HLSL 函式，包括頂點著色器、圖元著色器和 helper 函式。</span><span class="sxs-lookup"><span data-stu-id="9d0cc-129">The syntax on this page describes almost every type of HLSL function, this includes vertex shaders, pixel shaders, and helper functions.</span></span> <span data-ttu-id="9d0cc-130">雖然幾何著色器也會使用函式來執行，但其語法有點複雜，因此有個別的頁面可定義幾何著色器函式宣告 (請參閱 [幾何著色器物件 (DIRECTX HLSL) ](dx-graphics-hlsl-geometry-shader.md)) 。</span><span class="sxs-lookup"><span data-stu-id="9d0cc-130">While a geometry shader is also implemented with a function, its syntax is a little more complicated, so there is a separate page that defines a geometry shader function declaration (see [Geometry-Shader Object (DirectX HLSL)](dx-graphics-hlsl-geometry-shader.md)).</span></span>

<span data-ttu-id="9d0cc-131">只要指定了參數類型和/或參數順序的唯一組合，就可以多載函式。</span><span class="sxs-lookup"><span data-stu-id="9d0cc-131">A function can be overloaded as long as it is given a unique combination of parameter types and/or parameter order.</span></span> <span data-ttu-id="9d0cc-132">HLSL 也會執行一些內建或 [**內建函式**](dx-graphics-hlsl-intrinsic-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="9d0cc-132">HLSL also implements a number of built in, or [**intrinsic functions**](dx-graphics-hlsl-intrinsic-functions.md).</span></span>

<span data-ttu-id="9d0cc-133">您可以使用 **clipplanes** 屬性來指定使用者特定的剪輯平面。</span><span class="sxs-lookup"><span data-stu-id="9d0cc-133">You can specify user-specific clip planes with the **clipplanes** attribute.</span></span> <span data-ttu-id="9d0cc-134">Windows 會將這些剪輯平面套用至所有繪製的基本專案。</span><span class="sxs-lookup"><span data-stu-id="9d0cc-134">Windows applies these clip planes to all of the primitives drawn.</span></span> <span data-ttu-id="9d0cc-135">**Clipplanes** 屬性的運作方式類似 [SV \_ ClipDistance](dx-graphics-hlsl-semantics.md) ，但適用于所有硬體 [功能層級](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)9 \_ x 和更高。</span><span class="sxs-lookup"><span data-stu-id="9d0cc-135">The **clipplanes** attribute works like [SV\_ClipDistance](dx-graphics-hlsl-semantics.md) but works on all hardware [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span> <span data-ttu-id="9d0cc-136">如需詳細資訊，請參閱「 [功能等級9硬體上的使用者剪輯平面](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9)」。</span><span class="sxs-lookup"><span data-stu-id="9d0cc-136">For more info, see [User clip planes on feature level 9 hardware](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9).</span></span>

## <a name="examples"></a><span data-ttu-id="9d0cc-137">範例</span><span class="sxs-lookup"><span data-stu-id="9d0cc-137">Examples</span></span>

<span data-ttu-id="9d0cc-138">此範例來自 [BasicHLSL10 範例](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)中的 BasicHLSL10。</span><span class="sxs-lookup"><span data-stu-id="9d0cc-138">This example is from BasicHLSL10.fx from the [BasicHLSL10 Sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).</span></span>


```hlsl
struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; 
    float4 Diffuse    : COLOR0;
    float2 TextureUV  : TEXCOORD0;
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
    VS_OUTPUT Output;
    ...
    return Output;    
}
```



<span data-ttu-id="9d0cc-139">此範例來自 [AdvancedParticles 範例](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx)中的 AdvancedParticles，說明如何使用傳回型別的語義。</span><span class="sxs-lookup"><span data-stu-id="9d0cc-139">This example from AdvancedParticles.fx from the [AdvancedParticles Sample](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx), illustrates using a semantic for the return type.</span></span>


```hlsl
//
// PS for particles
//
float4 PSPointSprite(PSSceneIn input) : SV_Target
{   
    return g_txDiffuse.Sample( g_samLinear, input.tex ) * input.color;
}
```



## <a name="related-topics"></a><span data-ttu-id="9d0cc-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="9d0cc-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d0cc-141"> (DirectX HLSL) 的函式 </span><span class="sxs-lookup"><span data-stu-id="9d0cc-141">Functions (DirectX HLSL)</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 

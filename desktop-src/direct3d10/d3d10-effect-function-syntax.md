---
description: 效果函式是以 HLSL 撰寫，並且使用下列語法來宣告。
ms.assetid: 5ac85f09-50ac-4e8f-b4d2-ae8306b59348
title: " (Direct3D 10) 的效果函數語法"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88521eeb85d1e5f54500a045fe5dcfd81d6be2cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468185"
---
# <a name="effect-function-syntax-direct3d-10"></a><span data-ttu-id="4758f-103"> (Direct3D 10) 的效果函數語法</span><span class="sxs-lookup"><span data-stu-id="4758f-103">Effect Function Syntax (Direct3D 10)</span></span>

<span data-ttu-id="4758f-104">效果函式是以 HLSL 撰寫，並且使用下列語法來宣告。</span><span class="sxs-lookup"><span data-stu-id="4758f-104">An effect function is written in HLSL and is declared with the following syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="4758f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4758f-105">Syntax</span></span>

<span data-ttu-id="4758f-106">*ReturnType* *FunctionName* ( \[ *ArgumentList* \] ) </span><span class="sxs-lookup"><span data-stu-id="4758f-106">*ReturnType* *FunctionName* ( \[ *ArgumentList* \] )</span></span>

<span data-ttu-id="4758f-107">{</span><span class="sxs-lookup"><span data-stu-id="4758f-107">{</span></span>

<dl> <span data-ttu-id="4758f-108">\[ *陳述式* \]</span><span class="sxs-lookup"><span data-stu-id="4758f-108">\[ *Statements* \]</span></span>
</dl>

<span data-ttu-id="4758f-109">};</span><span class="sxs-lookup"><span data-stu-id="4758f-109">};</span></span>



| <span data-ttu-id="4758f-110">Name</span><span class="sxs-lookup"><span data-stu-id="4758f-110">Name</span></span>         | <span data-ttu-id="4758f-111">描述</span><span class="sxs-lookup"><span data-stu-id="4758f-111">Description</span></span>                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4758f-112">ReturnType</span><span class="sxs-lookup"><span data-stu-id="4758f-112">ReturnType</span></span>   | <span data-ttu-id="4758f-113">任何 [HLSL 類型](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md)</span><span class="sxs-lookup"><span data-stu-id="4758f-113">Any [HLSL type](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md)</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="4758f-114">FunctionName</span><span class="sxs-lookup"><span data-stu-id="4758f-114">FunctionName</span></span> | <span data-ttu-id="4758f-115">能唯一識別著色器函式名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="4758f-115">An ASCII string that uniquely identifies the name of the shader function.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="4758f-116">ArgumentList</span><span class="sxs-lookup"><span data-stu-id="4758f-116">ArgumentList</span></span> | <span data-ttu-id="4758f-117">以逗號分隔的一或多個引數 (請參閱 [ (DIRECTX HLSL) ](../direct3dhlsl/dx-graphics-hlsl-function-parameters.md)) 的函式引數。</span><span class="sxs-lookup"><span data-stu-id="4758f-117">One or more arguments, separated by commas (see [Function Arguments (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-function-parameters.md)).</span></span>                                                                                                                             |
| <span data-ttu-id="4758f-118">陳述式</span><span class="sxs-lookup"><span data-stu-id="4758f-118">Statements</span></span>   | <span data-ttu-id="4758f-119">一或多個語句 (查看組成函式主體 [ (DIRECTX HLSL) ](../direct3dhlsl/dx-graphics-hlsl-statements.md)) 的語句。</span><span class="sxs-lookup"><span data-stu-id="4758f-119">One or more statements (see [Statements (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-statements.md)) that make up the body of the function.</span></span> <span data-ttu-id="4758f-120">如果定義的函式沒有主體，則會被視為原型;和必須在使用之前以主體重新定義。</span><span class="sxs-lookup"><span data-stu-id="4758f-120">If a function is defined without a body, it is considered to be a prototype; and must be redefined with a body before use.</span></span> |



 

<span data-ttu-id="4758f-121">效果函式可能是著色器，也可能只是著色器所呼叫的函式。</span><span class="sxs-lookup"><span data-stu-id="4758f-121">An effect function may be a shader or it may simply be a function called by a shader.</span></span> <span data-ttu-id="4758f-122">函式是由其名稱、其參數的類型和目標平臺來唯一識別;因此，可以多載函式。</span><span class="sxs-lookup"><span data-stu-id="4758f-122">A function is uniquely identified by its name, the types of its parameters, and the target platform; therefore, functions can be overloaded.</span></span> <span data-ttu-id="4758f-123">任何有效的 HLSL 函式都應該符合此格式;如需 HLSL 函式的語法詳細清單，請參閱) 的函式 [ (DIRECTX HLSL ](../direct3dhlsl/dx-graphics-hlsl-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="4758f-123">Any valid HLSL function should fit this format; for a more detailed list of syntax for HLSL functions, see [Functions (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-functions.md).</span></span>

## <a name="example"></a><span data-ttu-id="4758f-124">範例</span><span class="sxs-lookup"><span data-stu-id="4758f-124">Example</span></span>

<span data-ttu-id="4758f-125">[BasicHLSL10 範例](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)會使用圖元著色器和頂點著色器。</span><span class="sxs-lookup"><span data-stu-id="4758f-125">The [BasicHLSL10 sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) uses both a pixel shader and a vertex shader.</span></span> <span data-ttu-id="4758f-126">圖元著色器函式稱為 RenderScenePS，如下所示。</span><span class="sxs-lookup"><span data-stu-id="4758f-126">The pixel shader function is called RenderScenePS and is shown below.</span></span>


```
       
PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                         uniform bool bTexture ) 
{ 
    PS_OUTPUT Output;

    // Lookup mesh texture and modulate it with diffuse
    if( bTexture )
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) *  
                              In.Diffuse;
    else
        Output.RGBColor = In.Diffuse;

    return Output;
}
```



## <a name="related-topics"></a><span data-ttu-id="4758f-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="4758f-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4758f-128">效果格式</span><span class="sxs-lookup"><span data-stu-id="4758f-128">Effect Format</span></span>](d3d10-effect-format.md)
</dt> </dl>

 

 

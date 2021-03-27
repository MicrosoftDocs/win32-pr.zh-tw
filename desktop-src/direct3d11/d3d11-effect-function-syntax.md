---
title: " (Direct3D 11) 的效果函數語法"
description: 效果函式是以 HLSL 撰寫，並使用本節所述的語法來宣告。
ms.assetid: 5e12ba65-98bf-4f21-be75-602687157eb1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f569211d5f178b96cf7415478010285e7a836b58
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682377"
---
# <a name="effect-function-syntax-direct3d-11"></a><span data-ttu-id="78ae2-103"> (Direct3D 11) 的效果函數語法</span><span class="sxs-lookup"><span data-stu-id="78ae2-103">Effect Function Syntax (Direct3D 11)</span></span>

<span data-ttu-id="78ae2-104">效果函式是以 HLSL 撰寫，並使用本節所述的語法來宣告。</span><span class="sxs-lookup"><span data-stu-id="78ae2-104">An effect function is written in HLSL and is declared with the syntax described in this section.</span></span>

## <a name="syntax"></a><span data-ttu-id="78ae2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="78ae2-105">Syntax</span></span>

<span data-ttu-id="78ae2-106">*ReturnType* *FunctionName* ( \[ *ArgumentList* \] ) </span><span class="sxs-lookup"><span data-stu-id="78ae2-106">*ReturnType* *FunctionName* ( \[ *ArgumentList* \] )</span></span>

<span data-ttu-id="78ae2-107">{</span><span class="sxs-lookup"><span data-stu-id="78ae2-107">{</span></span>

<dl> <span data-ttu-id="78ae2-108">\[ *陳述式* \]</span><span class="sxs-lookup"><span data-stu-id="78ae2-108">\[ *Statements* \]</span></span>
</dl>

<span data-ttu-id="78ae2-109">};</span><span class="sxs-lookup"><span data-stu-id="78ae2-109">};</span></span>



| <span data-ttu-id="78ae2-110">名稱</span><span class="sxs-lookup"><span data-stu-id="78ae2-110">Name</span></span>         | <span data-ttu-id="78ae2-111">描述</span><span class="sxs-lookup"><span data-stu-id="78ae2-111">Description</span></span>                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78ae2-112">ReturnType</span><span class="sxs-lookup"><span data-stu-id="78ae2-112">ReturnType</span></span>   | <span data-ttu-id="78ae2-113">任何 [HLSL 類型](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)</span><span class="sxs-lookup"><span data-stu-id="78ae2-113">Any [HLSL type](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="78ae2-114">FunctionName</span><span class="sxs-lookup"><span data-stu-id="78ae2-114">FunctionName</span></span> | <span data-ttu-id="78ae2-115">能唯一識別著色器函式名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="78ae2-115">An ASCII string that uniquely identifies the name of the shader function.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="78ae2-116">ArgumentList</span><span class="sxs-lookup"><span data-stu-id="78ae2-116">ArgumentList</span></span> | <span data-ttu-id="78ae2-117">以逗號分隔的一或多個引數 (請參閱 [ (DIRECTX HLSL) ](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters)) 的函式引數。</span><span class="sxs-lookup"><span data-stu-id="78ae2-117">One or more arguments, separated by commas (see [Function Arguments (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters)).</span></span>                                                                                                                             |
| <span data-ttu-id="78ae2-118">陳述式</span><span class="sxs-lookup"><span data-stu-id="78ae2-118">Statements</span></span>   | <span data-ttu-id="78ae2-119">一或多個語句 (查看組成函式主體 [ (DIRECTX HLSL) ](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-statements)) 的語句。</span><span class="sxs-lookup"><span data-stu-id="78ae2-119">One or more statements (see [Statements (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-statements)) that make up the body of the function.</span></span> <span data-ttu-id="78ae2-120">如果定義的函式沒有主體，則會被視為原型;和必須在使用之前以主體重新定義。</span><span class="sxs-lookup"><span data-stu-id="78ae2-120">If a function is defined without a body, it is considered to be a prototype; and must be redefined with a body before use.</span></span> |



 

<span data-ttu-id="78ae2-121">效果函式可能是著色器，也可能只是著色器所呼叫的函式。</span><span class="sxs-lookup"><span data-stu-id="78ae2-121">An effect function may be a shader or it may simply be a function called by a shader.</span></span> <span data-ttu-id="78ae2-122">函式是由其名稱、其參數的類型和目標平臺來唯一識別;因此，可以多載函式。</span><span class="sxs-lookup"><span data-stu-id="78ae2-122">A function is uniquely identified by its name, the types of its parameters, and the target platform; therefore, functions can be overloaded.</span></span> <span data-ttu-id="78ae2-123">任何有效的 HLSL 函式都應該符合此格式;如需 HLSL 函式的語法詳細清單，請參閱) 的函式 [ (DIRECTX HLSL ](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-functions)。</span><span class="sxs-lookup"><span data-stu-id="78ae2-123">Any valid HLSL function should fit this format; for a more detailed list of syntax for HLSL functions, see [Functions (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-functions).</span></span>

## <a name="example"></a><span data-ttu-id="78ae2-124">範例</span><span class="sxs-lookup"><span data-stu-id="78ae2-124">Example</span></span>

<span data-ttu-id="78ae2-125">以下是圖元著色器函式的範例。</span><span class="sxs-lookup"><span data-stu-id="78ae2-125">The following is an example of a pixel shader function.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="78ae2-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="78ae2-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78ae2-127">效果格式</span><span class="sxs-lookup"><span data-stu-id="78ae2-127">Effect Format</span></span>](d3d11-effect-format.md)
</dt> </dl>

 

 
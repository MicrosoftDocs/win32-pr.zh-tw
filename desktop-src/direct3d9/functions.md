---
description: 函式是以高階語言建立之著色器的組建區塊。 如果您想要以 C 樣式的語言撰寫著色器，而不是以組合語言撰寫，您會想要撰寫函數。
ms.assetid: vs|directx_sdk|~\functions.htm
title: " (Direct3D 9) 的效果函數語法"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21e239359877813e64acea8b5f404a6ade59c992
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509888"
---
# <a name="effect-function-syntax-direct3d-9"></a><span data-ttu-id="b14a3-104"> (Direct3D 9) 的效果函數語法</span><span class="sxs-lookup"><span data-stu-id="b14a3-104">Effect Function Syntax (Direct3D 9)</span></span>

<span data-ttu-id="b14a3-105">函式是以高階語言建立之著色器的組建區塊。</span><span class="sxs-lookup"><span data-stu-id="b14a3-105">A function is the building block for a shader created in the high-level language.</span></span> <span data-ttu-id="b14a3-106">如果您想要以 C 樣式的語言撰寫著色器，而不是以組合語言撰寫，您會想要撰寫函數。</span><span class="sxs-lookup"><span data-stu-id="b14a3-106">If you prefer to write shaders in a C-style language instead of in assembly language, you will want to write functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="b14a3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b14a3-107">Syntax</span></span>


```
type id ( [ parameters ] )  
    { body }
```



<span data-ttu-id="b14a3-108">函數不會變更效果中的參數值。</span><span class="sxs-lookup"><span data-stu-id="b14a3-108">Functions do not change parameter values in an effect.</span></span>

-   <span data-ttu-id="b14a3-109">type-HLSL 型別的任何有效 [參考](../direct3dhlsl/dx-graphics-hlsl-reference.md) 。</span><span class="sxs-lookup"><span data-stu-id="b14a3-109">type - Any valid [Reference for HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) type.</span></span>
-   <span data-ttu-id="b14a3-110">識別碼-唯一的名稱。</span><span class="sxs-lookup"><span data-stu-id="b14a3-110">id - A unique name.</span></span>
-   <span data-ttu-id="b14a3-111">參數函數參數。</span><span class="sxs-lookup"><span data-stu-id="b14a3-111">parameters - Function parameters.</span></span>
-   <span data-ttu-id="b14a3-112">body-函式的主體。</span><span class="sxs-lookup"><span data-stu-id="b14a3-112">body - The body of the function.</span></span>

<span data-ttu-id="b14a3-113">函式是從高階語言建立的。</span><span class="sxs-lookup"><span data-stu-id="b14a3-113">Functions are built from the high-level language.</span></span> <span data-ttu-id="b14a3-114">請參閱 [HLSL 的參考](../direct3dhlsl/dx-graphics-hlsl-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="b14a3-114">See [Reference for HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b14a3-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="b14a3-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b14a3-116">效果格式</span><span class="sxs-lookup"><span data-stu-id="b14a3-116">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 

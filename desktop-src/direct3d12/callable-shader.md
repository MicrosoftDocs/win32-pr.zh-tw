---
description: 從具有 CallShader 內建的另一個著色器叫用的著色器。
ms.assetid: ''
title: 可呼叫著色器
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- Callable Shader
api_type:
- NA
ms.openlocfilehash: 65df547c5e40a46cc4c35361b88ceb797c2e8852
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106984546"
---
# <a name="callable-shader"></a><span data-ttu-id="39656-103">可呼叫著色器</span><span class="sxs-lookup"><span data-stu-id="39656-103">Callable Shader</span></span>

<span data-ttu-id="39656-104">從具有 [**CallShader**](callshader-function.md) 內建的另一個著色器叫用的著色器。</span><span class="sxs-lookup"><span data-stu-id="39656-104">A shader that is invoked from another shader with the [**CallShader**](callshader-function.md) intrinsic.</span></span>

<span data-ttu-id="39656-105">**CallShader** 呼叫位置提供的參數結構必須符合要求索引所指向之可呼叫著色器中所使用的參數結構，以供透過 [**DispatchRays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays)方法提供的可呼叫著色器資料表使用。</span><span class="sxs-lookup"><span data-stu-id="39656-105">There is a parameter structure supplied at the **CallShader** call site that must match the parameter structure used in the callable shader pointed to by the requested index into the callable shader table supplied through the [**DispatchRays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) method.</span></span>  <span data-ttu-id="39656-106">可呼叫的著色器必須將此參數宣告為 *inout*。</span><span class="sxs-lookup"><span data-stu-id="39656-106">The callable shader must declare this parameter as *inout*.</span></span>  <span data-ttu-id="39656-107">此外，可呼叫的著色器可能會讀取啟動索引和維度輸入。</span><span class="sxs-lookup"><span data-stu-id="39656-107">Additionally, the callable shader may read launch index and dimension inputs.</span></span> <span data-ttu-id="39656-108">如需詳細資訊，請參閱 [**系統值內建函式**](direct3d-12-raytracing-hlsl-system-value-intrinsics.md)。</span><span class="sxs-lookup"><span data-stu-id="39656-108">For more information, see [**System Value Intrinsics**](direct3d-12-raytracing-hlsl-system-value-intrinsics.md).</span></span> 


## <a name="shader-type-attribute"></a><span data-ttu-id="39656-109">著色器類型屬性</span><span class="sxs-lookup"><span data-stu-id="39656-109">Shader Type attribute</span></span>


```
[shader("callable")]
```



## <a name="example"></a><span data-ttu-id="39656-110">範例</span><span class="sxs-lookup"><span data-stu-id="39656-110">Example</span></span>

```
[shader("callable")]
void callable_main(inout MyParams params)
{
    // Perform some common operations and update params
    CallShader( ... );  // maybe
}

```

 

 





---
description: 從著色器中叫用另一個著色器。
ms.assetid: ''
title: CallShader 函式
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- CallShader
api_type:
- NA
ms.openlocfilehash: 8c5cdf4e0a71430d6375fd75ca553f92ca9539b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972335"
---
# <a name="callshader-function"></a><span data-ttu-id="d1b09-103">CallShader 函式</span><span class="sxs-lookup"><span data-stu-id="d1b09-103">CallShader function</span></span>

<span data-ttu-id="d1b09-104">從著色器中叫用另一個著色器。</span><span class="sxs-lookup"><span data-stu-id="d1b09-104">Invokes another shader from within a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1b09-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1b09-105">Syntax</span></span>
<span data-ttu-id="d1b09-106">此內建函式定義相當於下列函式範本：</span><span class="sxs-lookup"><span data-stu-id="d1b09-106">This intrinsic function definition is equivalent to the following function template:</span></span>

```
template<param_t>
void CallShader(uint ShaderIndex, inout param_t Parameter);
```



## <a name="parameters"></a><span data-ttu-id="d1b09-107">參數</span><span class="sxs-lookup"><span data-stu-id="d1b09-107">Parameters</span></span>

`ShaderIndex`

<span data-ttu-id="d1b09-108">不帶正負號的整數，表示在 [**DispatchRays**] 的呼叫中指定之可呼叫 [著色器](callable-shader.md)資料表的索引， (/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays。</span><span class="sxs-lookup"><span data-stu-id="d1b09-108">An unsigned integer representing the index into the [callable shader](callable-shader.md) table specified in the call to [**DispatchRays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays.</span></span>

`Parameter`

<span data-ttu-id="d1b09-109">要傳遞至可呼叫著色器的使用者定義參數。</span><span class="sxs-lookup"><span data-stu-id="d1b09-109">The user-defined parameters to pass to the callable shader.</span></span>  <span data-ttu-id="d1b09-110">這個參數結構必須符合著色器資料表中所指的可呼叫著色器所使用的參數結構。</span><span class="sxs-lookup"><span data-stu-id="d1b09-110">This parameter structure must match the parameter structure used in the callable shader pointed to in the shader table.</span></span>


## <a name="return-value"></a><span data-ttu-id="d1b09-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d1b09-111">Return Value</span></span>

<span data-ttu-id="d1b09-112">**void**</span><span class="sxs-lookup"><span data-stu-id="d1b09-112">**void**</span></span>

## <a name="remarks"></a><span data-ttu-id="d1b09-113">備註</span><span class="sxs-lookup"><span data-stu-id="d1b09-113">Remarks</span></span>

<span data-ttu-id="d1b09-114">您可以從下列 raytracing 著色器類型呼叫這個函數：</span><span class="sxs-lookup"><span data-stu-id="d1b09-114">This function can be called from the following raytracing shader types:</span></span>

* [<span data-ttu-id="d1b09-115">**可呼叫著色器**</span><span class="sxs-lookup"><span data-stu-id="d1b09-115">**Callable Shader**</span></span>](callable-shader.md)
* [<span data-ttu-id="d1b09-116">**最接近的點擊著色器**</span><span class="sxs-lookup"><span data-stu-id="d1b09-116">**Closest Hit Shader**</span></span>](closest-hit-shader.md)
* [<span data-ttu-id="d1b09-117">**遺漏著色器**</span><span class="sxs-lookup"><span data-stu-id="d1b09-117">**Miss Shader**</span></span>](miss-shader.md)
* [<span data-ttu-id="d1b09-118">**光線產生著色器**</span><span class="sxs-lookup"><span data-stu-id="d1b09-118">**Ray Generation Shader**</span></span>](ray-generation-shader.md)



## <a name="see-also"></a><span data-ttu-id="d1b09-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1b09-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1b09-120">Direct3D 12 Raytracing HLSL 參考</span><span class="sxs-lookup"><span data-stu-id="d1b09-120">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 





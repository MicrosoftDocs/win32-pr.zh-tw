---
title: WaveActiveAllTrue 函式
description: 如果目前 wave 的所有作用中通道中的運算式為 true，則傳回 true。
ms.assetid: C4EC5A02-6070-4FF4-B855-F597FFFE66F0
keywords:
- WaveActiveAllTrue 函式 HLSL
topic_type:
- apiref
api_name:
- WaveActiveAllTrue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a26e0ce757257d6fdd8296239dcf086bff5f1666
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104463921"
---
# <a name="waveactivealltrue-function"></a><span data-ttu-id="91882-104">WaveActiveAllTrue 函式</span><span class="sxs-lookup"><span data-stu-id="91882-104">WaveActiveAllTrue function</span></span>

<span data-ttu-id="91882-105">如果目前 wave 的所有作用中通道中的運算式為 true，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="91882-105">Returns true if the expression is true in all active lanes in the current wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="91882-106">語法</span><span class="sxs-lookup"><span data-stu-id="91882-106">Syntax</span></span>

``` syntax
bool WaveActiveAllTrue(
   bool expr
);
```

## <a name="parameters"></a><span data-ttu-id="91882-107">參數</span><span class="sxs-lookup"><span data-stu-id="91882-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91882-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="91882-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="91882-109">要評估的布林運算式。</span><span class="sxs-lookup"><span data-stu-id="91882-109">The boolean expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91882-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="91882-110">Return value</span></span>

<span data-ttu-id="91882-111">如果運算式在所有泳道中為 true，則為 true。</span><span class="sxs-lookup"><span data-stu-id="91882-111">True if the expression is true in all lanes.</span></span>

## <a name="remarks"></a><span data-ttu-id="91882-112">備註</span><span class="sxs-lookup"><span data-stu-id="91882-112">Remarks</span></span>

<span data-ttu-id="91882-113">所有著色器階段中的著色器模型6.0 都支援此函數。</span><span class="sxs-lookup"><span data-stu-id="91882-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="91882-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91882-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91882-115">著色器模型6總覽</span><span class="sxs-lookup"><span data-stu-id="91882-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="91882-116">著色器模型6</span><span class="sxs-lookup"><span data-stu-id="91882-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 





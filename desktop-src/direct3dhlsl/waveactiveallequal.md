---
title: WaveActiveAllEqual 函式
description: 如果目前 wave (中的每個使用中通道的運算式相同，則會傳回 true，因此) 之間保持一致。
ms.assetid: E0A051A8-0ADD-4EC7-8D9A-8820CED9DA9D
keywords:
- WaveActiveAllEqual 函式 HLSL
topic_type:
- apiref
api_name:
- WaveActiveAllEqual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 34745e428fcd4453ce7274fc2a5accc6185f5b10
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103684232"
---
# <a name="waveactiveallequal-function"></a><span data-ttu-id="7511f-104">WaveActiveAllEqual 函式</span><span class="sxs-lookup"><span data-stu-id="7511f-104">WaveActiveAllEqual function</span></span>

<span data-ttu-id="7511f-105">如果目前 wave (中的每個使用中通道的運算式相同，則會傳回 true，因此) 之間保持一致。</span><span class="sxs-lookup"><span data-stu-id="7511f-105">Returns true if the expression is the same for every active lane in the current wave (and thus uniform across it).</span></span>

## <a name="syntax"></a><span data-ttu-id="7511f-106">語法</span><span class="sxs-lookup"><span data-stu-id="7511f-106">Syntax</span></span>


``` syntax
bool WaveActiveAllEqual(
   <type> expr
);
```



## <a name="parameters"></a><span data-ttu-id="7511f-107">參數</span><span class="sxs-lookup"><span data-stu-id="7511f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7511f-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="7511f-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="7511f-109">要評估的運算式。</span><span class="sxs-lookup"><span data-stu-id="7511f-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7511f-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="7511f-110">Return value</span></span>

<span data-ttu-id="7511f-111">如果目前 wave 中的每個使用中通道的運算式相同，則為 True。</span><span class="sxs-lookup"><span data-stu-id="7511f-111">True if the expression is the same for every active lane in the current wave.</span></span>

## <a name="remarks"></a><span data-ttu-id="7511f-112">備註</span><span class="sxs-lookup"><span data-stu-id="7511f-112">Remarks</span></span>

<span data-ttu-id="7511f-113">所有著色器階段中的著色器模型6.0 都支援此函數。</span><span class="sxs-lookup"><span data-stu-id="7511f-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="7511f-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7511f-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7511f-115">著色器模型6總覽</span><span class="sxs-lookup"><span data-stu-id="7511f-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="7511f-116">著色器模型6</span><span class="sxs-lookup"><span data-stu-id="7511f-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 





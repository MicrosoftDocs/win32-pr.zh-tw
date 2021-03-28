---
title: WaveActiveMin 函式
description: 傳回在目前 wave 的所有作用中通道上，運算式的最小值，將它複製回所有使用中的通道。
ms.assetid: BA762C02-894C-4AF9-A226-C1E3AAC286FF
keywords:
- WaveActiveMin 函式 HLSL
topic_type:
- apiref
api_name:
- WaveActiveMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91555df354ab2b7ffc447a9422c4811ae23e6e0c
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104024326"
---
# <a name="waveactivemin-function"></a><span data-ttu-id="3dd5a-104">WaveActiveMin 函式</span><span class="sxs-lookup"><span data-stu-id="3dd5a-104">WaveActiveMin function</span></span>

<span data-ttu-id="3dd5a-105">傳回在目前 wave 的所有作用中通道上，運算式的最小值，將它複製回所有使用中的通道。</span><span class="sxs-lookup"><span data-stu-id="3dd5a-105">Returns the minimum value of the expression across all active lanes in the current wave replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dd5a-106">語法</span><span class="sxs-lookup"><span data-stu-id="3dd5a-106">Syntax</span></span>

``` syntax
<type> WaveActiveMin(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="3dd5a-107">參數</span><span class="sxs-lookup"><span data-stu-id="3dd5a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dd5a-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="3dd5a-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="3dd5a-109">要評估的運算式。</span><span class="sxs-lookup"><span data-stu-id="3dd5a-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dd5a-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="3dd5a-110">Return value</span></span>

<span data-ttu-id="3dd5a-111">最小值。</span><span class="sxs-lookup"><span data-stu-id="3dd5a-111">The minimum value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dd5a-112">備註</span><span class="sxs-lookup"><span data-stu-id="3dd5a-112">Remarks</span></span>

<span data-ttu-id="3dd5a-113">作業的順序未定義。</span><span class="sxs-lookup"><span data-stu-id="3dd5a-113">The order of operations is undefined.</span></span>

<span data-ttu-id="3dd5a-114">所有著色器階段中的著色器模型6.0 都支援此函數。</span><span class="sxs-lookup"><span data-stu-id="3dd5a-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="3dd5a-115">範例</span><span class="sxs-lookup"><span data-stu-id="3dd5a-115">Examples</span></span>

``` syntax
 float3 minPos = WaveActiveMin( myPoint.position );
    BoundingBox.min = min( minPos, BoundingBox.min );
```

## <a name="see-also"></a><span data-ttu-id="3dd5a-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3dd5a-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dd5a-117">著色器模型6總覽</span><span class="sxs-lookup"><span data-stu-id="3dd5a-117">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="3dd5a-118">著色器模型6</span><span class="sxs-lookup"><span data-stu-id="3dd5a-118">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 





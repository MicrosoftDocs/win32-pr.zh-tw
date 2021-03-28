---
title: WaveActiveMax 函式
description: 傳回目前 wave 中所有使用中通道的運算式的最大值，並將其複寫回所有使用中的通道。
ms.assetid: 19101C56-2618-4F34-8725-DF92198ABDA4
keywords:
- WaveActiveMax 函式 HLSL
topic_type:
- apiref
api_name:
- WaveActiveMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c0fd10f578d598c326cdfb4cf943d3a35fe78a9
ms.sourcegitcommit: a232805e6c618673f2df904111cc4f5a33e15504
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/07/2020
ms.locfileid: "104383385"
---
# <a name="waveactivemax-function"></a><span data-ttu-id="0fbd9-104">WaveActiveMax 函式</span><span class="sxs-lookup"><span data-stu-id="0fbd9-104">WaveActiveMax function</span></span>

<span data-ttu-id="0fbd9-105">傳回目前 wave 中所有使用中通道的運算式的最大值，並將其複寫回所有使用中的通道。</span><span class="sxs-lookup"><span data-stu-id="0fbd9-105">Returns the maximum value of the expression across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fbd9-106">語法</span><span class="sxs-lookup"><span data-stu-id="0fbd9-106">Syntax</span></span>

``` syntax
<type> WaveActiveMax(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="0fbd9-107">參數</span><span class="sxs-lookup"><span data-stu-id="0fbd9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fbd9-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="0fbd9-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="0fbd9-109">要評估的運算式。</span><span class="sxs-lookup"><span data-stu-id="0fbd9-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fbd9-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="0fbd9-110">Return value</span></span>

<span data-ttu-id="0fbd9-111">最大值。</span><span class="sxs-lookup"><span data-stu-id="0fbd9-111">The maximum value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fbd9-112">備註</span><span class="sxs-lookup"><span data-stu-id="0fbd9-112">Remarks</span></span>

<span data-ttu-id="0fbd9-113">作業的順序未定義。</span><span class="sxs-lookup"><span data-stu-id="0fbd9-113">The order of operations is undefined.</span></span>

<span data-ttu-id="0fbd9-114">所有著色器階段中的著色器模型6.0 都支援此函數。</span><span class="sxs-lookup"><span data-stu-id="0fbd9-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="0fbd9-115">範例</span><span class="sxs-lookup"><span data-stu-id="0fbd9-115">Examples</span></span>

``` syntax
 float3 maxPos = WaveActiveMax( myPoint.position );
    BoundingBox.max = max( maxPos, BoundingBox.max );
```

## <a name="see-also"></a><span data-ttu-id="0fbd9-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0fbd9-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fbd9-117">著色器模型6總覽</span><span class="sxs-lookup"><span data-stu-id="0fbd9-117">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="0fbd9-118">著色器模型6</span><span class="sxs-lookup"><span data-stu-id="0fbd9-118">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 





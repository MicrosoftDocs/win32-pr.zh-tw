---
title: WaveActiveBallot 函式
description: 傳回 uint4，其中包含目前 wave 中所有使用中通道的布林運算式評估的位元遮罩。
ms.assetid: 67FE28E0-F397-431A-8CF8-64E4AD88CDBC
keywords:
- WaveActiveBallot 函式 HLSL
topic_type:
- apiref
api_name:
- WaveActiveBallot
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3cdd89fad7da1e4ba7f3d5e032370834166a114
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104508196"
---
# <a name="waveactiveballot-function"></a><span data-ttu-id="e806e-104">WaveActiveBallot 函式</span><span class="sxs-lookup"><span data-stu-id="e806e-104">WaveActiveBallot function</span></span>

<span data-ttu-id="e806e-105">傳回 uint4，其中包含目前 wave 中所有使用中通道的布林運算式評估的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="e806e-105">Returns a uint4 containing a bitmask of the evaluation of the Boolean expression for all active lanes in the current wave.</span></span> 

## <a name="syntax"></a><span data-ttu-id="e806e-106">語法</span><span class="sxs-lookup"><span data-stu-id="e806e-106">Syntax</span></span>

``` syntax
uint4 WaveBallot(
   bool expr
);
```

## <a name="parameters"></a><span data-ttu-id="e806e-107">參數</span><span class="sxs-lookup"><span data-stu-id="e806e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e806e-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="e806e-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="e806e-109">要評估的布林運算式。</span><span class="sxs-lookup"><span data-stu-id="e806e-109">The boolean expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e806e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e806e-110">Return value</span></span>

<span data-ttu-id="e806e-111">Uint4，包含目前 wave 中所有使用中通道的布林運算式評估的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="e806e-111">A uint4 containing a bitmask of the evaluation of the Boolean expression for all active lanes in the current wave.</span></span> <span data-ttu-id="e806e-112">最不重要的位會對應至索引為零的通道。</span><span class="sxs-lookup"><span data-stu-id="e806e-112">The least-significant bit corresponds to the lane with index zero.</span></span> <span data-ttu-id="e806e-113">對應到非使用中通道的位將會是零。</span><span class="sxs-lookup"><span data-stu-id="e806e-113">The bits corresponding to inactive lanes will be zero.</span></span> <span data-ttu-id="e806e-114">大於或等於 [**WaveGetLaneCount**](wavegetlanecount.md) 的位將會是零。</span><span class="sxs-lookup"><span data-stu-id="e806e-114">The bits that are greater than or equal to [**WaveGetLaneCount**](wavegetlanecount.md) will be zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e806e-115">備註</span><span class="sxs-lookup"><span data-stu-id="e806e-115">Remarks</span></span>

<span data-ttu-id="e806e-116">不同的 Gpu 具有不同的 SIMD 處理器寬度， (航道計數) 。</span><span class="sxs-lookup"><span data-stu-id="e806e-116">Different GPUs have different SIMD processor widths (lane counts).</span></span> <span data-ttu-id="e806e-117">這些 **WaveXXX** 函數大多都能在 SIMD 電腦寬度隱藏的抽象層級上運作。</span><span class="sxs-lookup"><span data-stu-id="e806e-117">Most of these **WaveXXX** functions are able to operate at level of abstraction where SIMD machine width is concealed.</span></span> <span data-ttu-id="e806e-118">若要最大化跨 Gpu 的程式碼可攜性，請使用不依賴電腦寬度的內建函式。</span><span class="sxs-lookup"><span data-stu-id="e806e-118">To maximize portability of code across GPUs, use the intrinsics that don’t rely on machine width.</span></span> <span data-ttu-id="e806e-119">例如，使用：</span><span class="sxs-lookup"><span data-stu-id="e806e-119">For example, use:</span></span>

``` syntax
uint result = WaveActiveCountBits( bBit );
```

<span data-ttu-id="e806e-120">不要這樣撰寫：</span><span class="sxs-lookup"><span data-stu-id="e806e-120">Instead of:</span></span>

``` syntax
uint result = countbits( WaveActiveBallot( bBit ) );
```

<span data-ttu-id="e806e-121">所有著色器階段中的著色器模型6.0 都支援此函數。</span><span class="sxs-lookup"><span data-stu-id="e806e-121">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="e806e-122">範例</span><span class="sxs-lookup"><span data-stu-id="e806e-122">Examples</span></span>

``` syntax
// get a bitwise representation of the number of currently active lanes:
uint4 waveBits = WaveActiveBallot( true ); // convert to bits 
```

## <a name="see-also"></a><span data-ttu-id="e806e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e806e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e806e-124">著色器模型6總覽</span><span class="sxs-lookup"><span data-stu-id="e806e-124">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="e806e-125">著色器模型6</span><span class="sxs-lookup"><span data-stu-id="e806e-125">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 





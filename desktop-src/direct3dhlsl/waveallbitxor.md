---
title: WaveActiveBitXor 函式
description: 傳回目前 wave 中所有使用中通道的所有運算式值的位 XOR，然後將它複製回所有使用中的通道。
ms.assetid: A6807D17-1E6E-4997-AB52-32FAB5857219
keywords:
- WaveActiveBitXor 函式 HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e55ce8a43311f4f4c428e97bff1e107ab5c7038
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104024325"
---
# <a name="waveactivebitxor-function"></a><span data-ttu-id="bf610-104">WaveActiveBitXor 函式</span><span class="sxs-lookup"><span data-stu-id="bf610-104">WaveActiveBitXor function</span></span>

<span data-ttu-id="bf610-105">傳回目前 wave 中所有使用中通道的所有運算式值的位 XOR，然後將它複製回所有使用中的通道。</span><span class="sxs-lookup"><span data-stu-id="bf610-105">Returns the bitwise XOR of all the values of the expression across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf610-106">語法</span><span class="sxs-lookup"><span data-stu-id="bf610-106">Syntax</span></span>

``` syntax
<int_type> WaveActiveBitXor(
   <int_type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="bf610-107">參數</span><span class="sxs-lookup"><span data-stu-id="bf610-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf610-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="bf610-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="bf610-109">要評估的運算式。</span><span class="sxs-lookup"><span data-stu-id="bf610-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf610-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="bf610-110">Return value</span></span>

<span data-ttu-id="bf610-111">位 XOR 值。</span><span class="sxs-lookup"><span data-stu-id="bf610-111">The bitwise XOR value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf610-112">備註</span><span class="sxs-lookup"><span data-stu-id="bf610-112">Remarks</span></span>

<span data-ttu-id="bf610-113">所有著色器階段中的著色器模型6.0 都支援此函數。</span><span class="sxs-lookup"><span data-stu-id="bf610-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="bf610-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf610-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf610-115">著色器模型6總覽</span><span class="sxs-lookup"><span data-stu-id="bf610-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="bf610-116">著色器模型6</span><span class="sxs-lookup"><span data-stu-id="bf610-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 





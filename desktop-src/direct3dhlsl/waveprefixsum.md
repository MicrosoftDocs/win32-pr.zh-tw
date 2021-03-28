---
title: WavePrefixSum 函式
description: 傳回使用中通道的所有值加上小於此值的總和。
ms.assetid: F51B90AB-3E85-4521-8A2C-7C16A4ECB1F9
keywords:
- WavePrefixSum 函式 HLSL
topic_type:
- apiref
api_name:
- WavePrefixSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b133aa37b522156df73914eef66c4d3695a70ed7
ms.sourcegitcommit: 41c742c88f7d9ce05e107008f186b6e872ff9288
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/31/2021
ms.locfileid: "104973864"
---
# <a name="waveprefixsum-function"></a><span data-ttu-id="ad715-104">WavePrefixSum 函式</span><span class="sxs-lookup"><span data-stu-id="ad715-104">WavePrefixSum function</span></span>

<span data-ttu-id="ad715-105">傳回使用中通道的所有值加上小於此值的總和。</span><span class="sxs-lookup"><span data-stu-id="ad715-105">Returns the sum of all of the values in the active lanes with smaller indices than this one.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad715-106">語法</span><span class="sxs-lookup"><span data-stu-id="ad715-106">Syntax</span></span>

``` syntax
<type> WavePrefixSum(
   <type> value
);
```

## <a name="parameters"></a><span data-ttu-id="ad715-107">參數</span><span class="sxs-lookup"><span data-stu-id="ad715-107">Parameters</span></span>

<span data-ttu-id="ad715-108">*value*</span><span class="sxs-lookup"><span data-stu-id="ad715-108">*value*</span></span> 

<span data-ttu-id="ad715-109">要加總的值。</span><span class="sxs-lookup"><span data-stu-id="ad715-109">The value to sum up.</span></span>

## <a name="return-value"></a><span data-ttu-id="ad715-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="ad715-110">Return value</span></span>

<span data-ttu-id="ad715-111">值的總和。</span><span class="sxs-lookup"><span data-stu-id="ad715-111">The sum of the values.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad715-112">備註</span><span class="sxs-lookup"><span data-stu-id="ad715-112">Remarks</span></span>

<span data-ttu-id="ad715-113">無法保證此常式上的作業順序。</span><span class="sxs-lookup"><span data-stu-id="ad715-113">The order of operations on this routine cannot be guaranteed.</span></span> <span data-ttu-id="ad715-114">如此一來，就能有效地 \[ \] 在其中忽略精確的旗標。</span><span class="sxs-lookup"><span data-stu-id="ad715-114">So, effectively, the \[precise\] flag is ignored within it.</span></span>

<span data-ttu-id="ad715-115">您可以藉由將前置詞加總新增至目前通道的值來計算後置總和。</span><span class="sxs-lookup"><span data-stu-id="ad715-115">A postfix sum can be computed by adding the prefix sum to the current lane's value.</span></span>

<span data-ttu-id="ad715-116">請注意，具有最低索引的使用中通道一律會收到0的前置詞總和。</span><span class="sxs-lookup"><span data-stu-id="ad715-116">Note that the active lane with the lowest index will always receive a 0 for its prefix sum.</span></span>

<span data-ttu-id="ad715-117">所有著色器階段中的著色器模型6.0 都支援此函數。</span><span class="sxs-lookup"><span data-stu-id="ad715-117">This function is supported from shader model 6.0 in all shader stages.</span></span> 

## <a name="examples"></a><span data-ttu-id="ad715-118">範例</span><span class="sxs-lookup"><span data-stu-id="ad715-118">Examples</span></span>

```hlsl
uint numToSum = 2;
uint prefixSum = WavePrefixSum( numToSum );
```

<span data-ttu-id="ad715-119">在 wave 大小為8的電腦上，如果通道0和4以外的所有通道都在作用中，則會從 WavePrefixSum 傳回下列值。</span><span class="sxs-lookup"><span data-stu-id="ad715-119">On a machine with a wave size of 8, and all lanes active except lanes 0 and 4, the following values would be returned from WavePrefixSum.</span></span>

| <span data-ttu-id="ad715-120">通道索引</span><span class="sxs-lookup"><span data-stu-id="ad715-120">lane index</span></span> | <span data-ttu-id="ad715-121">status</span><span class="sxs-lookup"><span data-stu-id="ad715-121">status</span></span>   | <span data-ttu-id="ad715-122">prefixSum</span><span class="sxs-lookup"><span data-stu-id="ad715-122">prefixSum</span></span>     | 
|------------|----------|---------------|
| <span data-ttu-id="ad715-123">0</span><span class="sxs-lookup"><span data-stu-id="ad715-123">0</span></span>          | <span data-ttu-id="ad715-124">非使用中</span><span class="sxs-lookup"><span data-stu-id="ad715-124">inactive</span></span> | <span data-ttu-id="ad715-125">n/a</span><span class="sxs-lookup"><span data-stu-id="ad715-125">n/a</span></span>           |
| <span data-ttu-id="ad715-126">1</span><span class="sxs-lookup"><span data-stu-id="ad715-126">1</span></span>          | <span data-ttu-id="ad715-127">作用中</span><span class="sxs-lookup"><span data-stu-id="ad715-127">active</span></span>   | <span data-ttu-id="ad715-128">= 0</span><span class="sxs-lookup"><span data-stu-id="ad715-128">= 0</span></span>           |
| <span data-ttu-id="ad715-129">2</span><span class="sxs-lookup"><span data-stu-id="ad715-129">2</span></span>          | <span data-ttu-id="ad715-130">作用中</span><span class="sxs-lookup"><span data-stu-id="ad715-130">active</span></span>   | <span data-ttu-id="ad715-131">= 0 + 2</span><span class="sxs-lookup"><span data-stu-id="ad715-131">= 0+2</span></span>         |
| <span data-ttu-id="ad715-132">3</span><span class="sxs-lookup"><span data-stu-id="ad715-132">3</span></span>          | <span data-ttu-id="ad715-133">作用中</span><span class="sxs-lookup"><span data-stu-id="ad715-133">active</span></span>   | <span data-ttu-id="ad715-134">= 0 + 2 + 2</span><span class="sxs-lookup"><span data-stu-id="ad715-134">= 0+2+2</span></span>       |
| <span data-ttu-id="ad715-135">4</span><span class="sxs-lookup"><span data-stu-id="ad715-135">4</span></span>          | <span data-ttu-id="ad715-136">非使用中</span><span class="sxs-lookup"><span data-stu-id="ad715-136">inactive</span></span> | <span data-ttu-id="ad715-137">n/a</span><span class="sxs-lookup"><span data-stu-id="ad715-137">n/a</span></span>           |
| <span data-ttu-id="ad715-138">5</span><span class="sxs-lookup"><span data-stu-id="ad715-138">5</span></span>          | <span data-ttu-id="ad715-139">作用中</span><span class="sxs-lookup"><span data-stu-id="ad715-139">active</span></span>   | <span data-ttu-id="ad715-140">= 0 + 2 + 2 + 2</span><span class="sxs-lookup"><span data-stu-id="ad715-140">= 0+2+2+2</span></span>     |
| <span data-ttu-id="ad715-141">6</span><span class="sxs-lookup"><span data-stu-id="ad715-141">6</span></span>          | <span data-ttu-id="ad715-142">作用中</span><span class="sxs-lookup"><span data-stu-id="ad715-142">active</span></span>   | <span data-ttu-id="ad715-143">= 0 + 2 + 2 + 2 + 2</span><span class="sxs-lookup"><span data-stu-id="ad715-143">= 0+2+2+2+2</span></span>   |
| <span data-ttu-id="ad715-144">7</span><span class="sxs-lookup"><span data-stu-id="ad715-144">7</span></span>          | <span data-ttu-id="ad715-145">作用中</span><span class="sxs-lookup"><span data-stu-id="ad715-145">active</span></span>   | <span data-ttu-id="ad715-146">= 0 + 2 + 2 + 2 + 2 + 2</span><span class="sxs-lookup"><span data-stu-id="ad715-146">= 0+2+2+2+2+2</span></span> |

## <a name="see-also"></a><span data-ttu-id="ad715-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad715-147">See also</span></span>

[<span data-ttu-id="ad715-148">著色器模型6總覽</span><span class="sxs-lookup"><span data-stu-id="ad715-148">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[<span data-ttu-id="ad715-149">著色器模型6</span><span class="sxs-lookup"><span data-stu-id="ad715-149">Shader Model 6</span></span>](shader-model-6-0.md)

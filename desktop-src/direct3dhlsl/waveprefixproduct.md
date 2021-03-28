---
title: WavePrefixProduct 函式
description: 使用小於此通道的索引，傳回這個波中使用中通道內所有值的乘積。
ms.assetid: 3A5B271D-EF45-4511-9086-A9AD0D215D9A
keywords:
- WavePrefixProduct 函式 HLSL
topic_type:
- apiref
api_name:
- WavePrefixProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d073d72590951ddbbbb74274d4cd237e0a138c4f
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104383282"
---
# <a name="waveprefixproduct-function"></a><span data-ttu-id="544f5-104">WavePrefixProduct 函式</span><span class="sxs-lookup"><span data-stu-id="544f5-104">WavePrefixProduct function</span></span>

<span data-ttu-id="544f5-105">使用小於此通道的索引，傳回這個波中使用中通道內所有值的乘積。</span><span class="sxs-lookup"><span data-stu-id="544f5-105">Returns the product of all of the values in the active lanes in this wave with indices less than this lane.</span></span>

## <a name="syntax"></a><span data-ttu-id="544f5-106">語法</span><span class="sxs-lookup"><span data-stu-id="544f5-106">Syntax</span></span>

``` syntax
<type> WavePrefixProduct(
   <type> value
);
```

## <a name="parameters"></a><span data-ttu-id="544f5-107">參數</span><span class="sxs-lookup"><span data-stu-id="544f5-107">Parameters</span></span>

<span data-ttu-id="544f5-108">*value*</span><span class="sxs-lookup"><span data-stu-id="544f5-108">*value*</span></span> 

<span data-ttu-id="544f5-109">要相乘的值。</span><span class="sxs-lookup"><span data-stu-id="544f5-109">The value to multiply.</span></span>

## <a name="return-value"></a><span data-ttu-id="544f5-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="544f5-110">Return value</span></span>

<span data-ttu-id="544f5-111">所有值的乘積。</span><span class="sxs-lookup"><span data-stu-id="544f5-111">The product of all the values.</span></span>

## <a name="remarks"></a><span data-ttu-id="544f5-112">備註</span><span class="sxs-lookup"><span data-stu-id="544f5-112">Remarks</span></span>

<span data-ttu-id="544f5-113">無法保證此常式上的作業順序。</span><span class="sxs-lookup"><span data-stu-id="544f5-113">The order of operations on this routine cannot be guaranteed.</span></span> <span data-ttu-id="544f5-114">如此一來，就能有效地 \[ \] 在其中忽略精確的旗標。</span><span class="sxs-lookup"><span data-stu-id="544f5-114">So, effectively, the \[precise\] flag is ignored within it.</span></span>

<span data-ttu-id="544f5-115">您可以藉由將前置乘積乘以目前通道的值來計算後置產品。</span><span class="sxs-lookup"><span data-stu-id="544f5-115">A postfix product can be computed by multiplying the prefix product by the current lane's value.</span></span>

<span data-ttu-id="544f5-116">請注意，具有最低索引的使用中通道一律會收到其前置產品的1。</span><span class="sxs-lookup"><span data-stu-id="544f5-116">Note that the active lane with the lowest index will always receive a 1 for its prefix product.</span></span>

<span data-ttu-id="544f5-117">所有著色器階段中的著色器模型6.0 都支援此函數。</span><span class="sxs-lookup"><span data-stu-id="544f5-117">This function is supported from shader model 6.0 in all shader stages.</span></span> 

## <a name="examples"></a><span data-ttu-id="544f5-118">範例</span><span class="sxs-lookup"><span data-stu-id="544f5-118">Examples</span></span>

```hlsl
uint numToMultiply = 2;
uint prefixProduct = WavePrefixProduct( numToMultiply );
```

<span data-ttu-id="544f5-119">在 wave 大小為8的電腦上，如果通道0和4以外的所有通道都在作用中，則會從 WavePrefixProduct 傳回下列值。</span><span class="sxs-lookup"><span data-stu-id="544f5-119">On a machine with a wave size of 8, and all lanes active except lanes 0 and 4, the following values would be returned from WavePrefixProduct.</span></span>

| <span data-ttu-id="544f5-120">通道索引</span><span class="sxs-lookup"><span data-stu-id="544f5-120">lane index</span></span> | <span data-ttu-id="544f5-121">status</span><span class="sxs-lookup"><span data-stu-id="544f5-121">status</span></span>   | <span data-ttu-id="544f5-122">prefixProduct</span><span class="sxs-lookup"><span data-stu-id="544f5-122">prefixProduct</span></span> | 
|------------|----------|---------------|
| <span data-ttu-id="544f5-123">0</span><span class="sxs-lookup"><span data-stu-id="544f5-123">0</span></span>          | <span data-ttu-id="544f5-124">非使用中</span><span class="sxs-lookup"><span data-stu-id="544f5-124">inactive</span></span> | <span data-ttu-id="544f5-125">n/a</span><span class="sxs-lookup"><span data-stu-id="544f5-125">n/a</span></span>           |
| <span data-ttu-id="544f5-126">1</span><span class="sxs-lookup"><span data-stu-id="544f5-126">1</span></span>          | <span data-ttu-id="544f5-127">作用中</span><span class="sxs-lookup"><span data-stu-id="544f5-127">active</span></span>   | <span data-ttu-id="544f5-128"> = 1</span><span class="sxs-lookup"><span data-stu-id="544f5-128">= 1</span></span>           |
| <span data-ttu-id="544f5-129">2</span><span class="sxs-lookup"><span data-stu-id="544f5-129">2</span></span>          | <span data-ttu-id="544f5-130">作用中</span><span class="sxs-lookup"><span data-stu-id="544f5-130">active</span></span>   | <span data-ttu-id="544f5-131">= 1 \* 2</span><span class="sxs-lookup"><span data-stu-id="544f5-131">= 1\*2</span></span>        |
| <span data-ttu-id="544f5-132">3</span><span class="sxs-lookup"><span data-stu-id="544f5-132">3</span></span>          | <span data-ttu-id="544f5-133">作用中</span><span class="sxs-lookup"><span data-stu-id="544f5-133">active</span></span>   | <span data-ttu-id="544f5-134">= 1 \* 2 \* 2</span><span class="sxs-lookup"><span data-stu-id="544f5-134">= 1\*2\*2</span></span>     |
| <span data-ttu-id="544f5-135">4</span><span class="sxs-lookup"><span data-stu-id="544f5-135">4</span></span>          | <span data-ttu-id="544f5-136">非使用中</span><span class="sxs-lookup"><span data-stu-id="544f5-136">inactive</span></span> | <span data-ttu-id="544f5-137">n/a</span><span class="sxs-lookup"><span data-stu-id="544f5-137">n/a</span></span>           |
| <span data-ttu-id="544f5-138">5</span><span class="sxs-lookup"><span data-stu-id="544f5-138">5</span></span>          | <span data-ttu-id="544f5-139">作用中</span><span class="sxs-lookup"><span data-stu-id="544f5-139">active</span></span>   | <span data-ttu-id="544f5-140">= 1 \* 2 \* 2 2 \*</span><span class="sxs-lookup"><span data-stu-id="544f5-140">= 1\*2\*2\*2</span></span>       |
| <span data-ttu-id="544f5-141">6</span><span class="sxs-lookup"><span data-stu-id="544f5-141">6</span></span>          | <span data-ttu-id="544f5-142">作用中</span><span class="sxs-lookup"><span data-stu-id="544f5-142">active</span></span>   | <span data-ttu-id="544f5-143">= 1 \* 2 \* 2 \* 2 \* 2</span><span class="sxs-lookup"><span data-stu-id="544f5-143">= 1\*2\*2\*2\*2</span></span>    |
| <span data-ttu-id="544f5-144">7</span><span class="sxs-lookup"><span data-stu-id="544f5-144">7</span></span>          | <span data-ttu-id="544f5-145">作用中</span><span class="sxs-lookup"><span data-stu-id="544f5-145">active</span></span>   | <span data-ttu-id="544f5-146">= 1 2 2 2 2 2 2 \* \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="544f5-146">= 1\*2\*2\*2\*2\*2</span></span> |

## <a name="see-also"></a><span data-ttu-id="544f5-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="544f5-147">See also</span></span>

[<span data-ttu-id="544f5-148">著色器模型6總覽</span><span class="sxs-lookup"><span data-stu-id="544f5-148">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[<span data-ttu-id="544f5-149">著色器模型6</span><span class="sxs-lookup"><span data-stu-id="544f5-149">Shader Model 6</span></span>](shader-model-6-0.md)

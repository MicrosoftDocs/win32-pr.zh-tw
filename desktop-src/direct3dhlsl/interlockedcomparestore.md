---
title: 'InterlockedCompareStore 函式 (HLSL 參考) '
description: 以不可部分完成的方式將目的地與比較值進行比較。 如果兩者相同，則會以輸入值覆寫目的地。
ms.assetid: eaf7e669-5240-40c9-9840-f4e7916e51b4
keywords:
- InterlockedCompareStore 函式 HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareStore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df3ffb51bbe8fe8150d19a390e62640e64ded5c9
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2020
ms.locfileid: "104374231"
---
# <a name="interlockedcomparestore-function-hlsl-reference"></a><span data-ttu-id="f4978-105">InterlockedCompareStore 函式 (HLSL 參考) </span><span class="sxs-lookup"><span data-stu-id="f4978-105">InterlockedCompareStore function (HLSL reference)</span></span>

<span data-ttu-id="f4978-106">以不可部分完成的方式將目的地與比較值進行比較。</span><span class="sxs-lookup"><span data-stu-id="f4978-106">Atomically compares the destination to the comparison value.</span></span> <span data-ttu-id="f4978-107">如果兩者相同，則會以輸入值覆寫目的地。</span><span class="sxs-lookup"><span data-stu-id="f4978-107">If they are identical, the destination is overwritten with the input value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4978-108">語法</span><span class="sxs-lookup"><span data-stu-id="f4978-108">Syntax</span></span>

``` syntax
void InterlockedCompareStore(
  in R dest,
  in T compare_value,
  in T value
);
```

## <a name="parameters"></a><span data-ttu-id="f4978-109">參數</span><span class="sxs-lookup"><span data-stu-id="f4978-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4978-110">*目的地* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f4978-110">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4978-111">類型： **R**</span><span class="sxs-lookup"><span data-stu-id="f4978-111">Type: **R**</span></span>

<span data-ttu-id="f4978-112">目的地位址。</span><span class="sxs-lookup"><span data-stu-id="f4978-112">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="f4978-113">*比較 \_ 值* \[\]</span><span class="sxs-lookup"><span data-stu-id="f4978-113">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4978-114">類型： **T**</span><span class="sxs-lookup"><span data-stu-id="f4978-114">Type: **T**</span></span>

<span data-ttu-id="f4978-115">比較值。</span><span class="sxs-lookup"><span data-stu-id="f4978-115">The comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="f4978-116">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f4978-116">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4978-117">類型： **T**</span><span class="sxs-lookup"><span data-stu-id="f4978-117">Type: **T**</span></span>

<span data-ttu-id="f4978-118">輸入值。</span><span class="sxs-lookup"><span data-stu-id="f4978-118">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4978-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="f4978-119">Return value</span></span>

<span data-ttu-id="f4978-120">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f4978-120">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4978-121">備註</span><span class="sxs-lookup"><span data-stu-id="f4978-121">Remarks</span></span>

<span data-ttu-id="f4978-122">如果值相符，則以原子方式將 *dest* 所參考的值與 *dest* 所參考的位置 *值* 進行比較。 *\_*</span><span class="sxs-lookup"><span data-stu-id="f4978-122">Atomically compares the value referenced by *dest* with *compare\_value* and stores *value* in the location referenced by *dest* if the values match.</span></span> <span data-ttu-id="f4978-123">此作業只能在 **int** 或 **uint** 型別資源和共用記憶體變數上執行。</span><span class="sxs-lookup"><span data-stu-id="f4978-123">This operation can only be performed on **int** or **uint** typed resources and shared memory variables.</span></span> <span data-ttu-id="f4978-124">此函式有兩種可能的用途。</span><span class="sxs-lookup"><span data-stu-id="f4978-124">There are two possible uses for this function.</span></span> <span data-ttu-id="f4978-125">第一個是當 R 是共用記憶體變數型別時。</span><span class="sxs-lookup"><span data-stu-id="f4978-125">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="f4978-126">在此情況下，此函式會在 *dest* 所參考的共用記憶體暫存器上執行作業。</span><span class="sxs-lookup"><span data-stu-id="f4978-126">In this case, the function performs the operation on the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="f4978-127">第二個案例是 R 是資源變數類型。</span><span class="sxs-lookup"><span data-stu-id="f4978-127">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="f4978-128">在此案例中，此函式會在 *dest* 所參考的資源位置上執行作業。</span><span class="sxs-lookup"><span data-stu-id="f4978-128">In this scenario, the function performs the operation on the resource location referenced by *dest*.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="f4978-129">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="f4978-129">Minimum Shader Model</span></span>

<span data-ttu-id="f4978-130">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="f4978-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f4978-131">著色器模型</span><span class="sxs-lookup"><span data-stu-id="f4978-131">Shader Model</span></span>                                                                | <span data-ttu-id="f4978-132">支援</span><span class="sxs-lookup"><span data-stu-id="f4978-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="f4978-133">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="f4978-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="f4978-134">是</span><span class="sxs-lookup"><span data-stu-id="f4978-134">yes</span></span>       |



 

<span data-ttu-id="f4978-135">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="f4978-135">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="f4978-136">頂點</span><span class="sxs-lookup"><span data-stu-id="f4978-136">Vertex</span></span> | <span data-ttu-id="f4978-137">船體</span><span class="sxs-lookup"><span data-stu-id="f4978-137">Hull</span></span> | <span data-ttu-id="f4978-138">網域</span><span class="sxs-lookup"><span data-stu-id="f4978-138">Domain</span></span> | <span data-ttu-id="f4978-139">幾何</span><span class="sxs-lookup"><span data-stu-id="f4978-139">Geometry</span></span> | <span data-ttu-id="f4978-140">像素</span><span class="sxs-lookup"><span data-stu-id="f4978-140">Pixel</span></span> | <span data-ttu-id="f4978-141">計算</span><span class="sxs-lookup"><span data-stu-id="f4978-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|  <span data-ttu-id="f4978-142">x</span><span class="sxs-lookup"><span data-stu-id="f4978-142">x</span></span>     | <span data-ttu-id="f4978-143">x</span><span class="sxs-lookup"><span data-stu-id="f4978-143">x</span></span>    |  <span data-ttu-id="f4978-144">x</span><span class="sxs-lookup"><span data-stu-id="f4978-144">x</span></span>     |  <span data-ttu-id="f4978-145">x</span><span class="sxs-lookup"><span data-stu-id="f4978-145">x</span></span>       | <span data-ttu-id="f4978-146">x</span><span class="sxs-lookup"><span data-stu-id="f4978-146">x</span></span>     | <span data-ttu-id="f4978-147">x</span><span class="sxs-lookup"><span data-stu-id="f4978-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="f4978-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4978-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4978-149">內建函式</span><span class="sxs-lookup"><span data-stu-id="f4978-149">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="f4978-150">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="f4978-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 





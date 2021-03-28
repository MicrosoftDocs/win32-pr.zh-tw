---
title: 'InterlockedCompareExchange 函式 (HLSL 參考) '
description: 以原子方式將目的地與比較值進行比較。 如果兩者相同，則會以輸入值覆寫目的地。 原始值會設定為目的地的原始值。
ms.assetid: 85d1ba58-8e79-41cd-abd6-7ffff59839c7
keywords:
- InterlockedCompareExchange 函式 HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74bc189996752d754599bf4547e8baa4d9fb74cc
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2020
ms.locfileid: "104990882"
---
# <a name="interlockedcompareexchange-function-hlsl-reference"></a><span data-ttu-id="951bc-106">InterlockedCompareExchange 函式 (HLSL 參考) </span><span class="sxs-lookup"><span data-stu-id="951bc-106">InterlockedCompareExchange function (HLSL reference)</span></span>

<span data-ttu-id="951bc-107">以原子方式將目的地與比較值進行比較。</span><span class="sxs-lookup"><span data-stu-id="951bc-107">Atomically compares the destination with the comparison value.</span></span> <span data-ttu-id="951bc-108">如果兩者相同，則會以輸入值覆寫目的地。</span><span class="sxs-lookup"><span data-stu-id="951bc-108">If they are identical, the destination is overwritten with the input value.</span></span> <span data-ttu-id="951bc-109">原始值會設定為目的地的原始值。</span><span class="sxs-lookup"><span data-stu-id="951bc-109">The original value is set to the destination's original value.</span></span>

## <a name="syntax"></a><span data-ttu-id="951bc-110">語法</span><span class="sxs-lookup"><span data-stu-id="951bc-110">Syntax</span></span>

``` syntax
void InterlockedCompareExchange(
  in  R dest,
  in  T compare_value,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="951bc-111">參數</span><span class="sxs-lookup"><span data-stu-id="951bc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="951bc-112">*目的地* \[在\]</span><span class="sxs-lookup"><span data-stu-id="951bc-112">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="951bc-113">類型： **R**</span><span class="sxs-lookup"><span data-stu-id="951bc-113">Type: **R**</span></span>

<span data-ttu-id="951bc-114">目的地位址。</span><span class="sxs-lookup"><span data-stu-id="951bc-114">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="951bc-115">*比較 \_ 值* \[\]</span><span class="sxs-lookup"><span data-stu-id="951bc-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="951bc-116">類型： **T**</span><span class="sxs-lookup"><span data-stu-id="951bc-116">Type: **T**</span></span>

<span data-ttu-id="951bc-117">比較值。</span><span class="sxs-lookup"><span data-stu-id="951bc-117">The comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="951bc-118">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="951bc-118">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="951bc-119">類型： **T**</span><span class="sxs-lookup"><span data-stu-id="951bc-119">Type: **T**</span></span>

<span data-ttu-id="951bc-120">輸入值。</span><span class="sxs-lookup"><span data-stu-id="951bc-120">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="951bc-121">*原始 \_ 值* \[ 輸出\]</span><span class="sxs-lookup"><span data-stu-id="951bc-121">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="951bc-122">類型： **T**</span><span class="sxs-lookup"><span data-stu-id="951bc-122">Type: **T**</span></span>

<span data-ttu-id="951bc-123">原始的值。</span><span class="sxs-lookup"><span data-stu-id="951bc-123">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="951bc-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="951bc-124">Return value</span></span>

<span data-ttu-id="951bc-125">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="951bc-125">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="951bc-126">備註</span><span class="sxs-lookup"><span data-stu-id="951bc-126">Remarks</span></span>

<span data-ttu-id="951bc-127">以不可部分完成的方式，將 *dest* 所參考的值與 *compare \_ 值* 進行比較，如果值相符，則會將 *值* 儲存在 *dest* 所參考的位置中，並以 *原始 \_ 值* 傳回 *dest* 的原始值。</span><span class="sxs-lookup"><span data-stu-id="951bc-127">Atomically compares the value referenced by *dest* with *compare\_value*, stores *value* in the location referenced by *dest* if the values match, returns the original value of *dest* in *original\_value*.</span></span> <span data-ttu-id="951bc-128">此作業只能在 **int** 或 **uint** 型別資源和共用記憶體變數上執行。</span><span class="sxs-lookup"><span data-stu-id="951bc-128">This operation can only be performed on **int** or **uint** typed resources and shared memory variables.</span></span> <span data-ttu-id="951bc-129">此函式有兩種可能的用途。</span><span class="sxs-lookup"><span data-stu-id="951bc-129">There are two possible uses for this function.</span></span> <span data-ttu-id="951bc-130">第一個是當 R 是共用記憶體變數型別時。</span><span class="sxs-lookup"><span data-stu-id="951bc-130">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="951bc-131">在此情況下，此函式會在 *dest* 所參考的共用記憶體暫存器上執行作業。</span><span class="sxs-lookup"><span data-stu-id="951bc-131">In this case, the function performs the operation on the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="951bc-132">第二個案例是 R 是資源變數類型。</span><span class="sxs-lookup"><span data-stu-id="951bc-132">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="951bc-133">在此案例中，此函式會在 *dest* 所參考的資源位置上執行作業。</span><span class="sxs-lookup"><span data-stu-id="951bc-133">In this scenario, the function performs the operation on the resource location referenced by *dest*.</span></span> <span data-ttu-id="951bc-134">只有當 R 可讀取和寫入時，才能使用此作業。</span><span class="sxs-lookup"><span data-stu-id="951bc-134">This operation is only available when R is readable and writable.</span></span>

> [!Note]  
> <span data-ttu-id="951bc-135">如果您在 [**for**](dx-graphics-hlsl-for.md)或 [**while**](dx-graphics-hlsl-while.md)計算著色器迴圈中呼叫 **InterlockedCompareExchange** ，以便正確編譯，您必須在該迴圈中使用 [ **\[ 允許 \_ uav \_ 條件 \]** ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="951bc-135">If you call **InterlockedCompareExchange** in a [**for**](dx-graphics-hlsl-for.md) or [**while**](dx-graphics-hlsl-while.md) compute shader loop, to properly compile, you must use the **\[allow\_uav\_condition\]** attribute on that loop.</span></span>

 

### <a name="minimum-shader-model"></a><span data-ttu-id="951bc-136">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="951bc-136">Minimum Shader Model</span></span>

<span data-ttu-id="951bc-137">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="951bc-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="951bc-138">著色器模型</span><span class="sxs-lookup"><span data-stu-id="951bc-138">Shader Model</span></span>                                                                | <span data-ttu-id="951bc-139">支援</span><span class="sxs-lookup"><span data-stu-id="951bc-139">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="951bc-140">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="951bc-140">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="951bc-141">是</span><span class="sxs-lookup"><span data-stu-id="951bc-141">yes</span></span>       |



 

<span data-ttu-id="951bc-142">下列著色器類型支援此函數：</span><span class="sxs-lookup"><span data-stu-id="951bc-142">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="951bc-143">頂點</span><span class="sxs-lookup"><span data-stu-id="951bc-143">Vertex</span></span> | <span data-ttu-id="951bc-144">船體</span><span class="sxs-lookup"><span data-stu-id="951bc-144">Hull</span></span> | <span data-ttu-id="951bc-145">網域</span><span class="sxs-lookup"><span data-stu-id="951bc-145">Domain</span></span> | <span data-ttu-id="951bc-146">幾何</span><span class="sxs-lookup"><span data-stu-id="951bc-146">Geometry</span></span> | <span data-ttu-id="951bc-147">像素</span><span class="sxs-lookup"><span data-stu-id="951bc-147">Pixel</span></span> | <span data-ttu-id="951bc-148">計算</span><span class="sxs-lookup"><span data-stu-id="951bc-148">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="951bc-149">x</span><span class="sxs-lookup"><span data-stu-id="951bc-149">x</span></span>      |  <span data-ttu-id="951bc-150">x</span><span class="sxs-lookup"><span data-stu-id="951bc-150">x</span></span>   |  <span data-ttu-id="951bc-151">x</span><span class="sxs-lookup"><span data-stu-id="951bc-151">x</span></span>     |  <span data-ttu-id="951bc-152">x</span><span class="sxs-lookup"><span data-stu-id="951bc-152">x</span></span>       | <span data-ttu-id="951bc-153">x</span><span class="sxs-lookup"><span data-stu-id="951bc-153">x</span></span>     | <span data-ttu-id="951bc-154">x</span><span class="sxs-lookup"><span data-stu-id="951bc-154">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="951bc-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="951bc-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="951bc-156">內建函式</span><span class="sxs-lookup"><span data-stu-id="951bc-156">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="951bc-157">著色器模型5</span><span class="sxs-lookup"><span data-stu-id="951bc-157">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




